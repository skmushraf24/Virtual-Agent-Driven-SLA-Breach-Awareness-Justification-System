# Virtual Agent–Driven SLA Breach Awareness & Justification System

This project aims to improve SLA governance by integrating ServiceNow Virtual Agent capabilities with SLA monitoring and justification tracking. The solution proactively notifies assignees before an SLA breach, captures acknowledgements and justifications, and provides management with meaningful reports and dashboards—all by leveraging native ServiceNow Administration features without custom scripting.

---

## Functional Scope Mapping (ServiceNow Native)

Based on the **Functional Scope**, here is how each requirement will be implemented using native ServiceNow features:

### 1. SLA Monitoring (80% Threshold)
* **Configuration**:
  * We will monitor the `task_sla` table.
  * An incident is flagged as "At Risk" when `Percentage elapsed` >= 80% and `Stage` = `In Progress`.
  * We can create a database view or a simple list view filter on the Incident table that joins with `task_sla` to display the SLA percentage and remaining time directly on the Incident form or list.

### 2. Proactive Notifications & Virtual Agent Entry Point
* **Configuration**:
  * **Trigger**: Flow Designer triggers when a `task_sla` record reaches 80% elapsed time.
  * **Notification**: Send an email/Slack/Teams notification to the `assigned_to` user of the Incident.
  * **VA Link**: The notification will include a deep link to the Virtual Agent topic. The URL format will be:
    `https://<instance-name>.service-now.com/$sn_va_web_client.do?sysparm_topic=<topic_sys_id>&sysparm_document_id=<incident_sys_id>`
    This automatically opens the chat and starts the specific SLA justification topic for that incident.

### 3. Security & Access Control (Assignee-Only Justification)
* **Configuration**:
  * In the **Virtual Agent Topic**, the first step will be a Script Action (using native VA variables, no custom script required beyond standard utility checks) to verify:
    `vaInputs.user == vaInputs.incident_record.assigned_to`
  * If the logged-in user is **not** the assignee:
    * The Virtual Agent will output: *"Access Denied: Only the assigned user of this incident ([Assignee Name]) is authorized to submit this SLA justification."*
    * The flow will terminate.
  * If they match, the flow proceeds.

### 4. Conversational Interaction & Acknowledgment Flow
* **Configuration** (Virtual Agent Designer):
  * **Prompt**: *"Incident [Number] has consumed [80%] of its SLA. Do you acknowledge this risk?"*
  * **Buttons**: `[Acknowledge & Justify]` or `[Resolve Incident Now]`.
  * **Justification Selection**: Prompt user with a Choice input containing:
    * *Awaiting Customer Action*
    * *Awaiting Third-Party Vendor*
    * *Complex Technical Investigation*
    * *Resource Constraint / High Workload*
    * *Other*
  * **Additional Details**: Prompt for a short text input.

### 5. Incident Update Automation (Work Notes & Audit History)
* **Configuration**:
  * Once the VA topic completes, it will update a record in a custom table `u_sla_justification` (or update fields on `task_sla`).
  * A native **Flow Designer** flow will trigger on the creation/update of this justification.
  * **Action**: Update the associated Incident record:
    * Set `Work notes` = *"SLA Breach Risk Acknowledged by [User] at [Time]. Justification Category: [Category]. Details: [Details]."*
  * This automatically logs the update in the Incident's activity stream, preserving a complete, tamper-proof audit history.

### 6. Reporting & Dashboards
We will build a **ServiceNow Dashboard** containing the following native reports:
1. **SLA Breach Risk Heatmap**: A list/bar chart of open incidents where SLA elapsed percentage is between 80% and 100%.
2. **Justification Compliance**: A donut chart showing the percentage of breached or at-risk SLAs that have an associated justification.
3. **Justification Categories**: A pie chart showing the distribution of justification reasons (e.g., how many are due to "Awaiting Customer").
4. **Pending Justifications**: A list view of breached SLAs (`Stage` = `Breached`) where no justification has been submitted.

---

## Delivery Options

Since we are working in a local development environment, we have two ways to proceed:

### Option 1: Detailed Configuration & Design Document (ServiceNow Blueprints)
We will generate a complete set of XML-compatible design specifications, Flow Designer configurations, Virtual Agent topic design maps, and Dashboard configuration guides.

### Option 2: Interactive Web Prototype (Highly Recommended)
We will build a premium, high-fidelity web application using **HTML, CSS (Vanilla), and JavaScript** that simulates:
1. **The Assignee Experience**: A simulated ServiceNow Portal where the user can view their incidents, see an SLA progress bar (turning red at 80%), receive a simulated Virtual Agent notification, and interact with the Virtual Agent chat (complete with security checks, acknowledgement buttons, and justification dropdowns).
2. **The Automation**: Showing how submitting the justification automatically appends a formatted entry to the Incident's **Work Notes** and activity history.
3. **The Manager Dashboard**: A beautiful, real-time dashboard displaying the four reports specified in the functional scope with interactive charts and filtering.

---

## User Review Required

> [!IMPORTANT]
> Please review the updated plan. We recommend **Option 2 (Interactive Web Prototype)** as it will allow you to interactively experience and demonstrate the entire functional scope (including the 80% SLA trigger, Virtual Agent chat, Work Notes updates, and the Manager Dashboard) directly in your browser.

---

## Open Questions

1. **Work Notes Visibility**: Should the automated Work Notes update be public (visible to the customer in the Portal) or internal-only (Work Notes)? *We have assumed internal-only (Work Notes) for security and internal accountability.*
2. **Validation**: If the assignee selects "Resolve Incident Now" in the Virtual Agent, should the VA prompt them to enter resolution notes and resolve the incident immediately?

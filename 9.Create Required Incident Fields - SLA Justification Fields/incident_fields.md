# Task 9: Create Required Incident Fields â€“ SLA Justification Fields

## Project Title

**Virtual Agent-Driven SLA Breach Awareness & Justification System**

---

# Introduction

To support SLA breach tracking and accountability, additional custom fields are created in the **Incident** table. These fields allow support agents to acknowledge SLA breaches, record the reason for the breach, provide detailed justifications, and identify incidents that are at risk of breaching their SLA.

These custom fields are later used by the Virtual Agent, Flow Designer, UI Policies, Reports, and Dashboards.

---

# Objective

Create custom Incident table fields required for capturing SLA breach information and configure predefined choice values for the SLA Breach Reason field.

---

# Navigation

**System Definition -> Tables**

Open the **Incident [incident]** table.

---

# Fields Created

| Field Label | Data Type | Purpose |
|-------------|-----------|---------|
| SLA Breach Reason | Choice | Stores the predefined reason for SLA breach |
| SLA Breach Justification | String | Stores the explanation provided by the assignee |
| SLA Acknowledgement | True/False | Indicates whether the SLA breach has been acknowledged |
| SLA At Risk | True/False | Indicates whether the Incident is approaching an SLA breach |

---

# SLA Breach Reason Choice Values

The following choice values were configured for the **SLA Breach Reason** field.

| Value |
|--------|
| Dependency on third party |
| Awaiting user response |
| Incorrect categorization |
| System outage |
| Approval delay |
| Other |

---

# Implementation Steps

## Step 1 - Open Incident Table

- Login to ServiceNow.
- Search for **Tables**.
- Navigate to:

**System Definition -> Tables**

- Open the **Incident** table.

---

## Step 2 - Create "SLA Breach Reason"

Configure the following:

| Property | Value |
|----------|-------|
| Label | SLA Breach Reason |
| Type | Choice |

Save the field.

---

## Step 3 - Configure Choice Values

Add the following values:

- Dependency on third party
- Awaiting user response
- Incorrect categorization
- System outage
- Approval delay
- Other

Save the choices.

---

## Step 4 - Create "SLA Breach Justification"

Configure the following:

| Property | Value |
|----------|-------|
| Label | SLA Breach Justification |
| Type | String |

> **Note:** Use the **String** data type only. Do **not** use **Journal Input**.

Save the field.

---

## Step 5 - Create "SLA Acknowledgement"

Configure the following:

| Property | Value |
|----------|-------|
| Label | SLA Acknowledgement |
| Type | True/False |

Save the field.

---

## Step 6 - Create "SLA At Risk"

Configure the following:

| Property | Value |
|----------|-------|
| Label | SLA At Risk |
| Type | True/False |

Save the field.

---

# Screenshots

## Figure 1 - Incident Table Navigation

**Description:** Navigate to System Definition -> Tables and open the Incident table.

<img width="1024" height="1024" alt="incident_table_nav_1782806629804" src="https://github.com/user-attachments/assets/ab341b3a-b6a0-4f12-8b27-1891dc78474c" />


---

## Figure 2 - SLA Breach Reason Field

**Description:** Create the choice field 'SLA Breach Reason'.
<img width="1024" height="1024" alt="sla_breach_reason_config_1782806647918" src="https://github.com/user-attachments/assets/ccf2feb4-80ab-4140-81fb-e952b2d2a4ec" />


---

## Figure 3 - Choice Values

**Description:** Predefined choice values configured for the field.

<img width="1024" height="1024" alt="choice_values_config_1782806665244" src="https://github.com/user-attachments/assets/e79b7539-44fb-406e-9d90-2dc32ea9bce4" />


---

## Figure 4 - SLA Breach Justification Field

**Description:** Create the string field 'SLA Breach Justification'.
<img width="1024" height="1024" alt="justification_field_config_1782806681831" src="https://github.com/user-attachments/assets/e889d99c-a98b-475d-a25b-31bcbe804314" />


---

## Figure 5 - SLA Acknowledgement Field

**Description:** Create the true/false field 'SLA Acknowledgement'.
<img width="1024" height="1024" alt="acknowledgement_field_config_1782806697180" src="https://github.com/user-attachments/assets/3b5a0c3e-5ec6-4a18-bd57-872d18ff2761" />


---

## Figure 6 - SLA At Risk Field

**Description:** Create the true/false field 'SLA At Risk'.
<img width="1024" height="1024" alt="at_risk_field_config_1782806711496" src="https://github.com/user-attachments/assets/6c2cc784-55db-4e02-9896-4bba53fa3cec" />


---

# Expected Result

- Four custom Incident fields are successfully created.
- SLA Breach Reason contains all required predefined values.
- SLA Breach Justification stores user explanations as text.
- SLA Acknowledgement records user confirmation.
- SLA At Risk identifies incidents approaching SLA breach.

---

# Benefits

- Structured SLA breach tracking.
- Improved accountability.
- Supports Virtual Agent conversations.
- Enables automated notifications.
- Facilitates reporting and dashboard creation.
- Enhances SLA governance.

---

# Outcome

The Incident table was successfully extended with custom SLA-related fields. These fields provide the required data for capturing SLA breach information, enabling automation, reporting, and proactive SLA management.

---

# Conclusion

The custom Incident fields establish the data foundation for the Virtual Agent-Driven SLA Breach Awareness & Justification System. They enable consistent recording of SLA breach information, improve operational transparency, and support effective SLA governance.


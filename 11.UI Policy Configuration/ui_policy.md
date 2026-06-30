# Task 11: UI Policy Configuration

## Project Title

**Virtual Agent–Driven SLA Breach Awareness & Justification System**

---

# Introduction

UI Policies in ServiceNow dynamically control the behavior of form fields without requiring scripting. They allow administrators to make fields mandatory, visible, or read-only based on specific conditions.

In this project, a UI Policy is configured to ensure that when an Incident is marked as **SLA At Risk**, users are required to provide the necessary SLA breach details before proceeding.

---

# Objective

Create a UI Policy that makes SLA-related fields visible and mandatory whenever the **SLA At Risk** field is set to **True**.

---

# Navigation

**System UI → UI Policies → New**

---

# UI Policy Configuration

| Property | Value |
|----------|-------|
| Table | Incident |
| Short Description | SLA Justification Policy |
| Active | True |
| On Load | True |
| Reverse if False | True |

---

# UI Policy Condition

Configure the following condition:

| Field | Operator | Value |
|-------|----------|-------|
| SLA At Risk | is | True |

This ensures that the policy is applied only when the Incident is identified as approaching an SLA breach.

---

# UI Policy Actions

Configure the following UI Policy Actions.

---

## Action 1 – SLA Breach Reason

| Property | Value |
|----------|-------|
| Field | SLA Breach Reason |
| Visible | True |
| Mandatory | True |
| Read Only | False |

---

## Action 2 – SLA Breach Justification

| Property | Value |
|----------|-------|
| Field | SLA Breach Justification |
| Visible | True |
| Mandatory | True |
| Read Only | False |

---

## Action 3 – SLA Acknowledgement

| Property | Value |
|----------|-------|
| Field | SLA Acknowledgement |
| Visible | True |
| Mandatory | False |
| Read Only | False |

---

# Implementation Steps

## Step 1

Navigate to:

**System UI → UI Policies**

Click **New**.

---

## Step 2

Configure the UI Policy.

- Table: Incident
- Active: True
- Reverse if False: True

Save the record.

---

## Step 3

Configure the Condition.

```
SLA At Risk = True
```

Save the UI Policy.

---

## Step 4

Create UI Policy Actions.

### SLA Breach Reason

- Visible = True
- Mandatory = True

---

### SLA Breach Justification

- Visible = True
- Mandatory = True

---

### SLA Acknowledgement

- Visible = True

Save all actions.

---

# Working Flow

1. Incident reaches 80% SLA.
2. Flow Designer updates **SLA At Risk = True**.
3. UI Policy is triggered.
4. SLA Breach Reason becomes mandatory.
5. SLA Breach Justification becomes mandatory.
6. SLA Acknowledgement becomes visible.
7. User submits the required SLA information.

---

# Screenshots

### Figure 1 – UI Policy Navigation

**Description:** Navigate to System UI → UI Policies in ServiceNow.

![UI Policy Navigation](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/ui_policies_navigation_1782809832269.jpg)

---

### Figure 2 – UI Policy Configuration

**Description:** Configure the general settings for 'SLA Justification Policy' on the Incident table.

![UI Policy Configuration](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/ui_policy_config_1782809851781.jpg)

---

### Figure 3 – UI Policy Condition

**Description:** Set the trigger condition to 'SLA At Risk is True'.

![UI Policy Condition](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/ui_policy_condition_1782809869396.jpg)

---

### Figure 4 – UI Policy Action – SLA Breach Reason

**Description:** Configure action to make the Choice field 'SLA Breach Reason' visible and mandatory.

![UI Policy Action - SLA Breach Reason](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/ui_action_reason_1782809889334.jpg)

---

### Figure 5 – UI Policy Action – SLA Breach Justification

**Description:** Configure action to make the String field 'SLA Breach Justification' visible and mandatory.

![UI Policy Action - SLA Breach Justification](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/ui_action_justification_1782809903364.jpg)

---

### Figure 6 – UI Policy Action – SLA Acknowledgement

**Description:** Configure action to make the True/False field 'SLA Acknowledgement' visible.

![UI Policy Action - SLA Acknowledgement](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/ui_action_acknowledgement_1782809921939.jpg)

---

# Expected Result

- SLA-related fields appear automatically.
- Mandatory fields prevent incomplete submissions.
- SLA acknowledgement is visible to the assignee.
- Data quality is improved.
- SLA justification is consistently captured.

---

# Benefits

- No scripting required.
- Better user experience.
- Mandatory SLA documentation.
- Improved SLA compliance.
- Enhanced data consistency.
- Supports Virtual Agent workflow.

---

# Outcome

The UI Policy was successfully configured. Whenever an Incident is marked as **SLA At Risk**, the required SLA justification fields become visible and mandatory, ensuring complete and accurate SLA breach documentation.

---

# Conclusion

The UI Policy automates form behavior based on SLA status and ensures that support agents provide the required information before resolving SLA-related incidents. This improves accountability and strengthens SLA governance using standard ServiceNow Administration features.

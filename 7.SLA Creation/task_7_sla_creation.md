# Task 7: SLA Creation

## Project Title

**Virtual Agentâ€“Driven SLA Breach Awareness & Justification System**

---

# Introduction

A Service Level Agreement (SLA) defines the expected time within which a service request or incident must be completed. In this project, an SLA is configured to monitor the resolution time of Incident records and support proactive SLA breach awareness using the ServiceNow Virtual Agent.

---

# Objective

Create an SLA Definition for Incident Resolution that monitors incidents during business hours and integrates with the Virtual Agent workflow.

---

# Navigation

**Service Level Management â†’ SLA Definitions**

Click **New** to create a new SLA Definition.

---

# SLA Configuration

| Property | Value |
|-----------|-------|
| Name | Incident Resolution - Virtual Agent Governance |
| Type | SLA |
| Target | Resolution |
| Table | Incident |
| Active | True |
| Duration Type | User Specified |
| Duration | 8 Hours |
| Schedule Source | SLA Definition |
| Schedule | IT Support Business Hours |

---

# Implementation Steps

## Step 1: Open SLA Definitions

- Log in to the ServiceNow instance.
- Search for **SLA** in the Application Navigator.
- Navigate to:

**Service Level Management â†’ SLA Definitions**

---

## Step 2: Create a New SLA

Click **New** and enter the following values:

- Name: **Incident Resolution - Virtual Agent Governance**
- Type: **SLA**
- Target: **Resolution**
- Table: **Incident**
- Active: **True**

---

## Step 3: Configure Duration

Configure the SLA timing.

- Duration Type: **User Specified**
- Duration: **8 Hours**
- Schedule Source: **SLA Definition**
- Schedule: **IT Support Business Hours**

Click **Submit** or **Update**.

---

# Screenshots

## Figure 1 â€“ SLA Definitions Navigation

Shows navigation to **Service Level Management â†’ SLA Definitions**.

![SLA Definitions Navigation](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/sla_definitions_navigation_1782754936561.png)

---

## Figure 2 â€“ SLA Definition Configuration

Shows the completed SLA Definition for the project.

![SLA Definition Configuration](/C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/sla_definition_config_1782754963088.png)

---

# Expected Result

- SLA Definition created successfully.
- SLA is active.
- SLA is attached to Incident records.
- Business Schedule is associated with the SLA.
- Resolution time is calculated using business hours.

---

# Benefits

- Automated SLA tracking.
- Accurate business-hour calculations.
- Proactive SLA monitoring.
- Better incident management.
- Supports Virtual Agent notifications.

---

# Outcome

The Incident Resolution SLA was successfully created and configured using the **IT Support Business Hours** schedule. The SLA will monitor incident resolution time and serve as the foundation for SLA awareness, notifications, and reporting.

---

# Conclusion

Creating the SLA Definition is an essential configuration step in the project. It enables ServiceNow to monitor Incident resolution times accurately, trigger SLA awareness processes, and improve overall SLA governance using standard ServiceNow Administration features.


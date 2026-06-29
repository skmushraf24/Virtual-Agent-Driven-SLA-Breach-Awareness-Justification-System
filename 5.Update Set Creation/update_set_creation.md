# Task 5: Update Set Creation

## Project Title

**Virtual Agent–Driven SLA Breach Awareness & Justification System**

---

# Introduction

An Update Set in ServiceNow is a mechanism used to capture and migrate configuration changes from one instance to another. It records customizations such as forms, fields, flows, UI policies, and other administrative configurations.

For this project, a dedicated Update Set named **Virtual Agent for SLA V1** was created to track all configurations related to the Virtual Agent–Driven SLA Breach Awareness & Justification System.

---

# Objective

Create and activate a new Update Set to capture all project-related configuration changes.

---

# Navigation

**System Update Sets → Local Update Sets**

---

# Procedure

### Step 1: Open Local Update Sets

1. Log in to the ServiceNow instance.
2. In the Application Navigator, search for **Update Set**.
3. Navigate to:

**System Update Sets → Local Update Sets**

---

### Step 2: Create a New Update Set

1. Click the **New** button.
2. Enter the following details:

| Field       | Value                    |
| ----------- | ------------------------ |
| Name        | Virtual Agent for SLA V1 |
| Application | Global                   |
| State       | In Progress              |

---

### Step 3: Make the Update Set Current

1. Click **Submit and Make Current**.
2. Verify that the newly created Update Set becomes the active Update Set.

---

# Expected Result

* A new Update Set named **Virtual Agent for SLA V1** is successfully created.
* The Update Set status is **In Progress**.
* The Update Set is marked as the current working Update Set.
* All subsequent configuration changes are automatically captured.

---

# Screenshots

### Screenshot 1 – Navigation to Local Update Sets

**Description:** Navigate to **System Update Sets → Local Update Sets** from the Application Navigator.

<img width="1024" height="1024" alt="servicenow_navigation_update_set_1782750076365" src="https://github.com/user-attachments/assets/cd1e40a4-3b81-4994-b7fc-09775a29e2c6" />


---

### Screenshot 2 – Creating the Update Set

**Description:** Create a new Update Set with the name **Virtual Agent for SLA V1** and click **Submit and Make Current**.

<img width="1024" height="1024" alt="servicenow_create_update_set_1782750091729" src="https://github.com/user-attachments/assets/b0a250f1-0fb7-4bcb-83ed-5b1296ed3612" />


---

# Outcome

The Update Set was successfully created and activated. All project configurations performed during the development of the Virtual Agent–Driven SLA Breach Awareness & Justification System will be stored within this Update Set, ensuring proper version control and easy migration between ServiceNow instances.

---

# Conclusion

Creating a dedicated Update Set is an essential first step in ServiceNow administration projects. It enables organized change management, simplifies deployment, and ensures that all customizations can be migrated safely and efficiently.

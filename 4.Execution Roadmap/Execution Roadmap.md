# Project Walkthrough: SLA Breach Awareness & Justification System

We have implemented an **Interactive Web Prototype** that simulates the entire lifecycle of the **Virtual Agent–Driven SLA Breach Awareness & Justification System**. It allows you to experience the system from the perspective of all three stakeholders across the 6 project phases.

---

## 📂 Project Structure

All files have been created in the local directory:
* **Web Prototype**: [index.html](file:///C:/Users/ADMIN/.gemini/antigravity/scratch/sla-justification-system/index.html)
* **Task Checklist**: [task.md](file:///C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/task.md)

---

## 🚀 How to Run the Prototype

1. Navigate to the project folder: `C:\Users\ADMIN\.gemini\antigravity\scratch\sla-justification-system`
2. Open the [index.html](file:///C:/Users/ADMIN/.gemini/antigravity/scratch/sla-justification-system/index.html) file in any modern web browser (Double-click or drag-and-drop the file into Chrome/Edge/Firefox).
3. (Optional) Run a local development server in that directory:
   ```powershell
   # In PowerShell
   cd C:\Users\ADMIN\.gemini\antigravity\scratch\sla-justification-system
   python -m http.server 8000
   ```
   Then open `http://localhost:8000` in your browser.

---

## 🕹️ How to Interact with the Simulator

The prototype features three main sections designed to showcase the system's capabilities:

### 1. The Phase Walkthrough (Left Sidebar)
Click through the 6 phases to see how the system is built:
* **Phase 1 (Planning)**: Focuses on business objectives and stakeholders.
* **Phase 2 (Backend Setup)**: Shows the SLA definitions and conditions.
* **Phase 3 (Flows & UI)**: Focuses on the Flow Designer logic and UI Policies.
* **Phase 4 (Virtual Agent)**: Highlights the interactive chat.
* **Phase 5 (Reporting)**: Displays the live SLA Governance Dashboard.
* **Phase 6 (Testing)**: Unlocks the **Automated Test Runner** at the bottom of the screen.

### 2. Role-Based Experiences (Top Bar)
Toggle between roles to see different views:
* **👤 IT Support Agent**: View your assigned incidents, see real-time SLA progress bars (turning orange/red at 80%+), and receive/chat with the Virtual Agent.
* **📊 IT Manager**: View the **SLA Governance Dashboard** with live KPI indicators, an SVG circular compliance donut, a justification category breakdown, and an active risk heatmap.
* **⚙️ ServiceNow Admin**: View the visual blueprints of the **SLA Definitions**, **Flow Designer nodes**, **Virtual Agent Topic Flowchart**, and **UI Policies**.

### 3. Simulation Control Panel (Bottom Bar)
* **⏳ Elapse Time (+15 mins)**: Increases the elapsed SLA percentage of all active incidents. When an incident hits 80%, a simulated **ServiceNow SLA Risk Alert** pops up with a link to launch the Virtual Agent.
* **🔄 Reset Simulator**: Resets the state of all incidents and chats.

---

## 🛡️ Interactive Test Scenarios (Phase 6)

Switch to **Phase 6** in the sidebar to reveal the automated test runner in the bottom bar:

1. **Happy Path Test**:
   * Simulates an incident reaching 80%.
   * Triggers a notification toast.
   * Launches the Virtual Agent.
   * Chats automatically to select **Complex Technical Investigation**, writes comments, and submits.
   * Shows the **Work Notes** automatically updating on the Incident record and the **Manager Dashboard** updating in real time.
2. **Security Test**:
   * Logs in as **Alice Smith** (a different support agent).
   * Triggers a notification for an incident assigned to **John Doe**.
   * Alice tries to access the Virtual Agent chat link.
   * The Virtual Agent performs a security check, displays **Access Denied**, and blocks the submission.

---

## 📊 Visual Mockup

A premium, dark-mode design mockup has been created to guide the implementation:
<img width="646" height="551" alt="image" src="https://github.com/user-attachments/assets/5792b06e-6b40-45b3-a4e7-67a45deb0729" />


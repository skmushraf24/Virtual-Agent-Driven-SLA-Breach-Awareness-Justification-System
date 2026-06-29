# Task 6: Create Business Schedule

## Project Title

**Virtual Agent–Driven SLA Breach Awareness & Justification System**

---

# Objective

The objective of this task is to create a Business Schedule in ServiceNow that defines the official working hours of the IT Support team. This schedule will later be associated with Service Level Agreements (SLAs) to ensure that SLA calculations are performed only during business hours.

---

# Navigation

**System Scheduler → Schedules → New**

---

# Schedule Configuration

| Property      | Value                                           |
| ------------- | ----------------------------------------------- |
| Schedule Name | IT Support Business Hours                       |
| Time Zone     | IST (Asia/Kolkata)                              |
| Description   | Business schedule for Virtual Agent SLA project |

Click **Submit** or **Save** after entering the schedule details.

---

# Schedule Entry Configuration

After creating the schedule, open the **Schedule Entries** related list and click **New**.

Configure the following values:

| Property     | Value                     |
| ------------ | ------------------------- |
| Name         | IT Support Business Hours |
| Show As      | Busy                      |
| Working Days | Monday – Friday           |
| Start Time   | 09:00 AM                  |
| End Time     | 06:00 PM                  |
| Repeats      | Every Weekday (Mon–Fri)   |

Click **Submit** to save the schedule entry.

---

# Implementation Steps

### Step 1: Navigate to Business Schedules

* Log in to the ServiceNow instance.
* Search for **Scheduler** in the Application Navigator.
* Open **System Scheduler → Schedules**.

**Result:** The Business Schedule module opens successfully.

---

### Step 2: Create Business Schedule

* Click **New**.
* Enter **IT Support Business Hours** as the schedule name.
* Select **IST (Asia/Kolkata)** as the time zone.
* Add a brief description.
* Click **Submit**.

**Result:** The business schedule is successfully created.

---

### Step 3: Configure Schedule Entries

* Open the created schedule.
* Under **Schedule Entries**, click **New**.
* Configure:

  * Monday–Friday
  * 09:00 AM to 06:00 PM
  * Show As = Busy
  * Repeat = Every Weekday (Mon–Fri)
* Click **Submit**.

**Result:** The working hours are successfully configured.

---

# Screenshots

## Figure 1 – Navigation to Business Schedules

Shows navigation to **System Scheduler → Schedules**.

![Navigation to Business Schedules](file:///C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/schedules_navigation_1782754275660.png)

---

## Figure 2 – Business Schedule Created

Displays the newly created **IT Support Business Hours** schedule.

![Business Schedule Created](file:///C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/schedule_created_1782754291427.png)

---

## Figure 3 – Schedule Entry Configuration

Shows the working days, working hours, and **Show As = Busy** configuration.

![Schedule Entry Configuration](file:///C:/Users/ADMIN/.gemini/antigravity/brain/364ecda7-e697-4299-be7b-ac69dfd42438/schedule_entry_config_1782754309576.png)

---

# Expected Outcome

* Business Schedule created successfully.
* Working days configured as Monday–Friday.
* Working hours set to 09:00 AM–06:00 PM.
* Schedule configured as Busy.
* Schedule is ready to be associated with Service Level Agreements.

---

# Benefits

* Accurate SLA calculations.
* SLA timers run only during business hours.
* Better incident response tracking.
* Improved SLA compliance.
* Standardized working-hour management.

---

# Conclusion

The Business Schedule **IT Support Business Hours** was successfully created and configured. The defined working hours will be used by ServiceNow SLAs to calculate response and resolution times accurately, ensuring reliable SLA monitoring for the Virtual Agent–Driven SLA Breach Awareness & Justification System.

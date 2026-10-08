# F3 — Appointment Scheduling and Status Tracking

**Source:** Functional
**Description:** The doctor can schedule appointments, view the daily list, and update the appointment state as the visit progresses.

**Scenario 1: Appointment scheduled**
Given a patient record exists and the doctor selects a valid date and time
When the doctor creates the appointment
Then the system stores it in the daily appointment list with status Scheduled

**Scenario 2: Status updated**
Given an appointment exists
When the doctor updates the status to Completed, Cancelled, or No-show
Then the system saves the new status and shows the updated state in the schedule

**Scenario 3: Invalid appointment attempt**
Given the doctor tries to save an appointment without selecting a patient or with an invalid time
When the save action is triggered
Then the system rejects the appointment and shows a validation error

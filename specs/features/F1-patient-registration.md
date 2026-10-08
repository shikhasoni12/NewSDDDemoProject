# F1 — Patient Registration

**Source:** Functional
**Description:** The doctor can create and maintain a complete patient profile so clinical records are accurate and searchable.

**Scenario 1: New patient created**
Given the doctor is on the patient registration screen and all required patient fields are entered
When the doctor saves the patient record
Then the system creates the patient profile and displays it in the patient record view

**Scenario 2: Existing patient updated**
Given the doctor opens an existing patient record
When the doctor updates contact or demographic details and saves
Then the system stores the updated information and reflects it in the patient profile

**Scenario 3: Required fields missing**
Given the doctor tries to save a patient record without a required field such as name, DOB, or gender
When the save action is triggered
Then the system blocks the save and highlights the missing required fields

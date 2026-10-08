# F8 — Single-User Secure Login

**Source:** Inferred from NFR
**Description:** The doctor must sign in securely before being allowed to access patient data and consultation records.

**Scenario 1: Successful login**
Given the doctor enters valid credentials
When the login form is submitted
Then the system authenticates the user and opens the application

**Scenario 2: Invalid credentials**
Given the doctor enters the wrong username or password
When the login form is submitted
Then the system rejects the login and displays an error message

**Scenario 3: Missing credentials**
Given the doctor leaves username or password blank
When the login form is submitted
Then the system blocks authentication and requests the missing fields

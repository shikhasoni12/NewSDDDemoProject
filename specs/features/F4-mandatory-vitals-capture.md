# F4 — Mandatory Vitals Capture

**Source:** Functional
**Description:** The doctor must record the minimum clinical vitals for every consultation so every visit has a valid baseline record.

**Scenario 1: Vitals recorded successfully**
Given a consultation is open
When the doctor enters valid temperature, blood pressure, and pulse values and saves
Then the system stores the vitals as part of the consultation

**Scenario 2: Mandatory vitals missing**
Given one or more required vitals are blank
When the doctor saves the consultation
Then the system prevents saving and requests the missing values

**Scenario 3: Invalid vitals values**
Given the doctor enters non-numeric or clearly invalid medical values
When the consultation is saved
Then the system rejects the input and asks for valid values before saving

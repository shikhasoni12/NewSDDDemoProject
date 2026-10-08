# F6 — Prescription Management and Print

**Source:** Functional
**Description:** The doctor can add medications with dosing details and generate a printable prescription that includes the essential consultation content.

**Scenario 1: Prescription created**
Given a consultation is open and the doctor enters medicine name, dosage, frequency, duration, and instructions
When the doctor saves the prescription
Then the system stores the medication list and makes it available for print

**Scenario 2: Incomplete medicine details**
Given the doctor enters a medication without required details
When the save action is triggered
Then the system rejects the medication entry and highlights the missing fields

**Scenario 3: Printable prescription generated**
Given a consultation includes patient details, vitals, diagnosis, and medications
When the doctor chooses to print the prescription
Then the system generates a printable version including the clinic header, patient details, vitals, diagnosis, medications, and footer/signature area

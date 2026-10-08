# F5 — Consultation Notes Capture

**Source:** Functional
**Description:** The doctor can record complaints and diagnosis during the consultation and attach them to the patient’s visit.

**Scenario 1: Complaints and diagnosis saved**
Given a valid patient consultation is open
When the doctor enters complaint notes and diagnosis and saves
Then the system stores those notes under that patient’s visit record

**Scenario 2: Visit linked to patient**
Given a consultation is created for a selected patient
When the doctor saves the encounter
Then the system associates the consultation with the correct patient history

**Scenario 3: No active patient selected**
Given the doctor attempts to save clinical notes without selecting a patient
When the save action is triggered
Then the system blocks the save and prompts the doctor to select a patient

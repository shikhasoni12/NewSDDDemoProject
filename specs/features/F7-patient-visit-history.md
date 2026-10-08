# F7 — Patient Visit History

**Source:** Functional
**Description:** The doctor can review prior visits for a patient, inspect earlier clinical information, and filter by date.

**Scenario 1: History displayed**
Given a patient has recorded prior consultations
When the doctor opens the patient history
Then the system shows the past visits and their details

**Scenario 2: Date filter applied**
Given a patient has visits on multiple dates
When the doctor selects a specific date or date range
Then the system displays only the visits that match the filter

**Scenario 3: No visits for selected date**
Given a patient has no records for the selected date
When the doctor applies the date filter
Then the system shows an empty state indicating there are no matching visits

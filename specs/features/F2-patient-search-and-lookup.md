# F2 — Patient Search and Lookup

**Source:** Functional
**Description:** The doctor can quickly locate a patient by name or phone number and open the correct record without manual browsing.

**Scenario 1: Search by name**
Given multiple patients are registered
When the doctor enters a patient’s name in the search field
Then the system returns matching patient records

**Scenario 2: Search by phone number**
Given the doctor knows the patient’s phone number
When the doctor searches by that number
Then the system returns the matching patient record if it exists

**Scenario 3: No match found**
Given the doctor searches for a patient who is not registered
When the search is executed
Then the system shows a no-results state and does not create a patient record automatically

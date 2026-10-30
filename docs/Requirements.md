# Functional & Non-functional Requirements

- Functional

| ID  | Requirement                                                        |
|-----|--------------------------------------------------------------------|
| FR1 | The system shall let the user select a bus stop from a map or search box. |
| FR2 | The system shall display the predicted arrival time of the next bus. |
| FR3 | The system shall display the scheduled time next to each prediction. |
| FR4 | The system shall display the scheduled arrival time next to each predicted arrival time. |
| FR5 | The system shall label each displayed time as either "Scheduled" or "Live estimate". |
| FR6 | The system shall recalculate predictions each time a new vehicle position is received. |
| FR7 | The system shall let the user save a bus stop as a favourite. |
| FR8 | The system shall notify the user when a bus is predicted to arrive at a favourite stop within a user-chosen number of minutes. |
| FR9 | The system shall let the user report that a bus did not arrive at the predicted time. |

- Non-functional

| ID  | Type | Requirement                                                  |
|-----|------|--------------------------------------------------------------|
| NFR1 | Performance | The predicted arrival times for a selected stop shall load within 2 seconds on a 4G connection. |
| NFR2 | Accuracy | For at least 80% of tested trips, the predicted arrival time shall be within ±3 minutes of the actual arrival time, measured over a 2-week test period. |
| NFR3 | Reliability | If no new vehicle position has been received for more than 2 minutes, the system shall show the scheduled time with a "Live data unavailable" message. |
| NFR4 | Usability | In a test with 5 first-time users, each user shall find the next bus at a chosen stop within 30 seconds. |
| NFR5 | Security | The system shall use the user's location only after the user grants permission and shall not store the user's location on the server. The system shall label each displayed time as either "Scheduled" or "Live estimate". |

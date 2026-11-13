# PART B : REQUIREMENTS

## B1 Functional Requirements

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

## B2 Non-functional Requirements

| ID  | Type | Requirement                                                  |
|-----|------|--------------------------------------------------------------|
| NFR1 | Performance | The predicted arrival times for a selected stop shall load within 2 seconds on a 4G connection. |
| NFR2 | Accuracy | For at least 80% of tested trips, the predicted arrival time shall be within ±3 minutes of the actual arrival time, measured over a 2-week test period. |
| NFR3 | Reliability | If no new vehicle position has been received for more than 2 minutes, the system shall show the scheduled time with a "Live data unavailable" message. |
| NFR4 | Usability | In a test with 5 first-time users, each user shall find the next bus at a chosen stop within 30 seconds. |
| NFR5 | Security | The system shall use the user's location only after the user grants permission and shall not store the user's location on the server. The system shall label each displayed time as either "Scheduled" or "Live estimate". |


## B3 User Stories

US1 (FR2, FR3) As a daily commuter, I want to see when the next two buses will arrive at my stop, so that I can decide whether to wait or walk to another route.

- AC1: Selecting a stop shows the predicted arrival time of the next two buses for each route serving that stop.
- AC2: If only one bus is still running on the route, one time is shown with the message "Last bus of the day".
- AC3: The times are shown in minutes (e.g. "4 min") and in clock time (e.g. "8:14 AM").

US2 (FR4, FR5) As a first-time rider, I want to know whether a time is scheduled or live, so that I know how much I can trust it.

- AC1: Every time on screen carries a "Scheduled" or "Live estimate" label.
- AC2: When live data is unavailable, all times for that route change to "Scheduled".

US3 (FR7, FR8) As a student who takes the same bus every morning, I want an alert before my bus arrives at my saved stop, so that I can leave home at the right time and wait less.

- AC1: The user can choose an alert time of 5, 10 or 15 minutes for a favourite stop.
- AC2: A notification is sent when the predicted arrival is equal to or less than the chosen time.
- AC3: No notification is sent if the user turned alerts off for that stop.

# Process Documentation - AiKita

## 🏃 Sprint: Basic Planning & Strategy
| Story ID  | EffortEst | Prio | Actual Time | Changes | Sprint |
|-----------|-----------|------|-------------|---------|--------|
| aikPlan01 | 3         | 1    | 13h          | 0       |   [Sprint1](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-1)   |
| aikPlan02 | 3         | 1    | 16h          | Timeline for meetings has to be adjusted to work demand. Depending on the planned task more frequent meetings are held. |  [Sprint2](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-2)   |
| aikSec03 |     3     |  2  |      20h     |    0    |   [Sprint3](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-3)   |
| aikSec04 |     5     |  2  |    10h     |   Code snipets reduced duration of task.   |   [Sprint4](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-4)   |
| aikCloud01 |     3     |  2  |    10h     |   Code snipets reduced duration of task.   |   [Sprint4](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-4)   |
| aikMvp4 |     3     |  2  |    2h     |     Code snipets reduced duration of task.   |   [Sprint4](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-4)    |
| aikUs04 |    3      |  1  |      6h     |        |   [Sprint5](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-5)   |
| aikUs06 |    3      |  2  |      4h     |        |   [Sprint5](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-5)   |
| aikCore03 |    3      |  2 |      5h     |        |   [Sprint5](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-5)   |
| aikData01 |    5      |  1 |      10h     |        |   [Sprint5](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-5)   |
| aikData02 |    8      |  3 |      10h     |        |   [Sprint5](https://github.com/riosarah/AiKita.Planning/blob/main/syp/sprints_overview.md#calendar-sprint-5)   |


---

## Completed User stories


## Planning and Strategies
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikPlan01 | 1    | Planning & Strategy | As a product manager, I want to create a roadmap to break development into clear milestones. | Milestones and goals are clearly defined. Work focus is dictated by a timeline with concrete deadlines. | 3 | 13 | 100% | |
| aikPlan02 | 1    | Planning & Strategy | As a product manager, I want to organize and design the project’s workflow to maximize efficiency. | Weekly meetings are set and responsibilities are defined. Responsibility for individual tasks is assigned. | 3 | 16 | 100% | |
| aikUs04 | 1    | Child Management | As a user, I want to manage child information (add, edit, delete) so my class list remains accurate. | The system must allow adding, modifying, and removing child records, with real-time UI updates. | 3 | 6 | 100% | |
| aikUs05 | 2    | Child Management | As a user, I want to search for a child by name, so I can quickly find their details. | Search results should be ranked by relevance. | 3 | 4 | 100% | |
| aikUs06 | 2    | Child Management | As a user, I want to add a new child, so the system stays up-to-date. | New child can be added and appears in the list. | 3 | 4 | 100 | |
| aikUs07 | 2    | Child Management | As a user, I want to record and view observations about a child. | Observations can be added and are retrievable after saving. | 3 | 4 | 100 | |


## MVP
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikMvp04 | 2  | Data Processing  | As a developer, I want to apply field-specific anonymization strategies to backend data access. | Email → hashed, names → initials, phone → masked (***-1234). | 3 | 2 | 100% | |
| aikMvp05 | 2  | Data Processing  | As a developer, I want to apply field-specific anonymization strategies to frontend data access. | Email → hashed, names → initials, phone → masked (***-1234). | 3 | 2 | 100% | |


## Core System (MVP+)
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikCore02 | 2   | Sync             | As a user, I want to sync my data to a remote database. | The .NET backend must store data in PostgreSQL and track sync events with logs. | 13 | 20 | 100% | |
| aikCore03 | 2   | Data Management  | As a user, I want to delete stored records. | Each entry must have a delete button with a confirmation prompt. | 3 | 5 | 100% | |

## Data Management & Reports 
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
| aikData01 | 1   | Child Management   | As a user, I want to manage child lists for better organization. | I can create, modify, and delete child lists. | 5 | 10 | 100% | |
| aikData02 | 3   | Progress Tracking  | As a user, I want to track and review a child's progress. | The system must allow logging and filtering of observations over time. | 8 | 10 | 100% | |

## Security & Validation
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
| aikSec03  | 2    | Security | As a user, I want file uploads to be validated. | JSON uploads must be schema-validated before processing. | 3 | 20 | 100% | |
| aikSec04  | 2    | Security | As an admin, I want audit logs to track data access. | The system must log all read/write actions for compliance. | 5 | 10 | 100% | |


## Cloud API + Admin
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
| aikCloud01 | 2   | API   | As a user, I want to log in securely to the database. | Authentication must use JWT with a refresh mechanism. | 3 | 10 | 100% | |


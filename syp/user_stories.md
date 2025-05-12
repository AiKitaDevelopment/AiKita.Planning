# AiKita User Stories

## Planning and Strategies
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|
| aikPlan01 | 1    | Planning & Strategy | As a product manager, I want to create a roadmap to break development into clear milestones. | Milestones and goals are clearly defined. Work focus is dictated by a timeline with concrete deadlines. | 3 | 13 |
| aikPlan02 | 1    | Planning & Strategy | As a product manager, I want to organize and design the project’s workflow to maximize efficiency. | Weekly meetings are set and responsibilities are defined. Responsibility for individual tasks is assigned. | 3 | 16 |

---

## User Focus
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|
| aikUs01 | 1    | UI/UX            | As a teacher, I want a clean and intuitive user interface, so I can navigate the application easily. | The UI must follow modern design principles and receive at least 80% positive usability feedback. | 13 | 20 | 75%
| aikUs02 | 3    | UI/UX            | As a user I want an accessible UI where I can adjust colors, font size and button size to my needs. | The UI must be adjustable by the user within a reasonable range, according to EU Accessibility regulations. | 8 | 6,5 | 75%
| aikUs03 | 4    | UI/UX            | As a user I want all graphs to be easily visible even as a user with light visual impairments.| Generated charts and graphs are adjustable by color and size. | 8 |
| aikUs04 | 1    | Child Management | As a teacher, I want to manage child information (add, edit, delete) so my class list remains accurate. | The system must allow adding, modifying, and removing child records, with real-time UI updates. | 3 |
| aikUs05 | 5    | Feedback         | As a teacher, I want to provide feedback on the application, so it can be continuously improved. | A feedback form must allow submission with categorization (bug, feature request, general). | 5 |
| aikUs06 | 2    | Child Management | As a teacher, I want to search for a child by name or ID, so I can quickly find their details. | Search results should be returned within 500ms, ranked by relevance. | 3 |

---

## MVP
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|
| aikMvp01 | 1  | UI/UX            | As a user, I want to launch the app and see a clear welcome screen, so I know it is working. | Tauri shell must load Angular UI within 3s and display app title with a description. | 3 |
| aikMvp02 | 1  | Forms            | As a user, I want structured forms with validation, so I can enter correct data without errors. | Forms must include validation for all fields and display clear error messages. | 2 |
| aikMvp03 | 1  | Data Processing  | As a user, I want to submit a form and receive anonymized data as a backup so I can review and store it securely. | A .NET endpoint must return anonymized JSON data (e.g., hashed emails, masked phone numbers) within 1s. | 5 |
| aikMvp04 | 2  | Data Processing  | As a developer, I want to apply field-specific anonymization strategies to backend data access. | Email → hashed, names → initials, phone → masked (***-1234). | 3 | 2 | 100%
| aikMvp05 | 2  | Data Processing  | As a developer, I want to apply field-specific anonymization strategies to frontend data access. | Email → hashed, names → initials, phone → masked (***-1234). | 3 | 2 | 100%
| aikMvp06 | 1  | Data Management  | As a user, I want to save and view anonymized data, so I can manage records efficiently. | Data should be saved via EF Core to SQLite, with a UI list for browsing entries. | 3 |
| aikMvp07 | 2  | Export           | As a user, I want to export selected records, so I can use them externally. | A Download button must export the selected entries in a structured format. | 2 |
| aikMvp08 | 3  | Export           | As a user, I want to export multiple records at once. | A checkbox UI must allow selecting multiple records for batch export. | 2 |

---

## Core System (MVP+)
| ID        | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status |
|-----------|------|-----------------|-------------|---------------------------------|--------|------|--------|
| aikCore01 | 1   | Dashboard        | As an admin, I want to view all submitted entries in a structured dashboard. | The admin UI must display stored entries with filtering, sorting, and pagination. | 5 |
| aikCore02 | 2   | Sync             | As a user, I want to sync my data to a remote database. | The .NET backend must store data in PostgreSQL and track sync events with logs. | 13 |
| aikCore03 | 2   | Data Management  | As a user, I want to delete stored records. | Each entry must have a delete button with a confirmation prompt. | 3 |
| aikCore04 | 2   | UI/UX            | As a user, I want a warning before closing the app with unsaved changes. | The app must show a confirmation dialog when unsaved changes exist. | 2 |
| aikCore05 | 4   | Dashboard        | As a user, I want to see my recent activity in a sidebar. | A sidebar must show a log of recent interactions (e.g., submissions, edits). | 5 |

---

## Data Management & Reports  
| ID        | Prio | Epic               | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status |
|-----------|------|--------------------|-------------|---------------------------------|--------|------|--------|
| aikData01 | 1   | Child Management   | As a user, I want to manage child lists for better organization. | I can create, modify, and delete child lists. | 5 |
| aikData02 | 3   | Progress Tracking  | As a user, I want to track and review a child's progress. | The system must allow logging and filtering of observations over time. | 8 |
| aikData03 | 4   | Reports            | As a user, I want to export child data into tables. | I can generate and download CSV or Excel files. | 2 |
| aikData04 | 4   | Reports            | As a user, I want to visualize child performance. | The system must generate charts and graphs from stored data. | 8 |

---

## Security & Validation
| ID        | Prio | Epic     | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status |
|-----------|------|---------|-------------|---------------------------------|--------|-------|--------|
| aikSec01  | 1    | Security | As a user, I want all sensitive data to be encrypted. | AES-256 encryption must be applied. | 21 |
| aikSec02  | 2    | Security | As a user, I want to anonymize or exclude personal data when exporting. | An option must allow exporting anonymized or full data. | 3 |
| aikSec03  | 2    | Security | As a user, I want file uploads to be validated. | JSON uploads must be schema-validated before processing. | 3 | 20
| aikSec04  | 2    | Security | As an admin, I want audit logs to track data access. | The system must log all read/write actions for compliance. | 5 | 10

---

## Cloud API + Admin
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status |
|-----------|------|-------|-------------|---------------------------------|--------| --------|------|
| aikCloud01 | 2   | API   | As a user, I want to log in securely to the database. | Authentication must use JWT with a refresh mechanism. | 3 | 10
| aikCloud02 | 2   | API   | As a user, I want to log in securely to the child managment system. | Authentication must use JWT with a refresh mechanism. | 3 |
| aikCloud03 | 3   | API   | As an admin, I want role-based user permissions. | The admin UI must allow assigning and modifying roles. | 5 |
| aikCloud04 | 3   | API   | As a user, I want my cloud data to be secure. | The API must enforce HTTPS and encrypt stored data. | 8 |

---


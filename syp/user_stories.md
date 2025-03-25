# AiKita User Stories

## User Focus
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort |
|---------|------|-----------------|-------------|---------------------------------|--------|
| aikUs01 | 1    | UI/UX            | As a teacher, I want a clean and intuitive user interface, so I can navigate the application easily. | The UI must follow modern design principles and receive at least 80% positive usability feedback. | 5 |
| aikUs02 | 1    | Child Management | As a teacher, I want to manage child information (add, edit, delete) so my class list remains accurate. | The system must allow adding, modifying, and removing child records, with real-time UI updates. | 2 |
| aikUs03 | 2    | Feedback         | As a teacher, I want to provide feedback on the application, so it can be continuously improved. | A feedback form must allow submission with categorization (bug, feature request, general). | 5 |
| aikUs04 | 1    | Child Management | As a teacher, I want to search for a child by name or ID, so I can quickly find their details. | Search results should be returned within 500ms, ranked by relevance. | 3 |

---

## MVP
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort |
|---------|------|-----------------|-------------|---------------------------------|--------|
| aikMvp01 | 1  | UI/UX            | As a user, I want to launch the app and see a clear welcome screen, so I know it is working. | Tauri shell must load Angular UI within 3s and display app title with a description. | 1 |
| aikMvp02 | 1  | Forms            | As a user, I want structured forms with validation, so I can enter correct data without errors. | Forms must include validation for all fields and display clear error messages. | 2 |
| aikMvp03 | 1  | Data Processing  | As a user, I want to submit a form and receive anonymized data, so I can review it securely. | A .NET endpoint must return anonymized JSON data (e.g., hashed emails, masked phone numbers) within 1s. | 3 |
| aikMvp04 | 2  | Data Processing  | As a developer, I want to apply field-specific anonymization strategies. | Email → hashed, names → initials, phone → masked (***-1234). | 2 |
| aikMvp05 | 1  | Data Management  | As a user, I want to save and view anonymized data, so I can manage records efficiently. | Data should be saved via EF Core to SQLite, with a UI list for browsing entries. | 3 |
| aikMvp06 | 2  | Export           | As a user, I want to export selected records as JSON, so I can use them externally. | A "Download JSON" button must export the selected entries in a structured format. | 2 |
| aikMvp07 | 3  | Export           | As a user, I want to export multiple records at once. | A checkbox UI must allow selecting multiple records for batch export. | 2 |

---

## Core System (MVP+)
| ID        | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort |
|-----------|------|-----------------|-------------|---------------------------------|--------|
| aikCore01 | 1   | Dashboard        | As an admin, I want to view all submitted entries in a structured dashboard. | The admin UI must display stored entries with filtering, sorting, and pagination. | 5 |
| aikCore02 | 2   | Sync             | As a user, I want to sync my data to a remote database. | The .NET backend must store data in PostgreSQL and track sync events with logs. | 5 |
| aikCore03 | 2   | Data Management  | As a user, I want to delete stored records. | Each entry must have a delete button with a confirmation prompt. | 2 |
| aikCore04 | 3   | UI/UX            | As a user, I want a warning before closing the app with unsaved changes. | The app must show a confirmation dialog when unsaved changes exist. | 2 |
| aikCore05 | 2   | Dashboard        | As a user, I want to see my recent activity in a sidebar. | A sidebar must show a log of recent interactions (e.g., submissions, edits). | 4 |

---

## Data Management & Reports  
| ID        | Prio | Epic               | User Story  | COS (Criteria of Satisfaction)  | Effort |
|-----------|------|--------------------|-------------|---------------------------------|--------|
| aikData01 | 2   | Child Management   | As a teacher, I want to manage child lists for better organization. | I can create, modify, and delete child lists. | 3 |
| aikData02 | 3   | Progress Tracking  | As a teacher, I want to track and review a child's progress. | The system must allow logging and filtering of observations over time. | 3 |
| aikData03 | 4   | Reports            | As a teacher, I want to export child data into tables. | I can generate and download CSV or Excel files. | 4 |
| aikData04 | 4   | Reports            | As a teacher, I want to visualize child performance. | The system must generate charts and graphs from stored data. | 5 |

---

## Security & Validation
| ID        | Prio | Epic     | User Story  | COS (Criteria of Satisfaction)  | Effort |
|-----------|------|---------|-------------|---------------------------------|--------|
| aikSec01  | 1    | Security | As a user, I want all sensitive data to be encrypted. | AES-256 encryption must be applied at field level. | 4 |
| aikSec02  | 2    | Security | As a user, I want to anonymize or exclude personal data when exporting. | An option must allow exporting anonymized or full data. | 3 |
| aikSec03  | 2    | Security | As a user, I want file uploads to be validated. | JSON uploads must be schema-validated before processing. | 3 |
| aikSec04  | 2    | Security | As an admin, I want audit logs to track data access. | The system must log all read/write actions for compliance. | 4 |

---

## Cloud API + Admin
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort |
|-----------|------|-------|-------------|---------------------------------|--------|
| aikCloud01 | 2   | API   | As a user, I want to log in securely. | Authentication must use JWT with a refresh mechanism. | 3 |
| aikCloud02 | 2   | API   | As an admin, I want role-based user permissions. | The admin UI must allow assigning and modifying roles. | 4 |
| aikCloud03 | 1   | API   | As a user, I want my cloud data to be secure. | The API must enforce HTTPS and encrypt stored data. | 4 |

---

## Quality Assurance & Performance
| ID      | Prio | Epic | User Story  | COS (Criteria of Satisfaction)  | Effort |
|--------|------|------|-------------|---------------------------------|--------|
| eduQA01 | 2   | QA   | As a QA engineer, I want automated tests. | At least 80% test coverage must be achieved. | 13 |
| eduQA02 | 1   | QA   | As a QA engineer, I want performance tests. | The app must handle 100 users with <2s response times. | 12 |
| eduQA03 | 3   | QA   | As a QA engineer, I want usability tests. | Usability tests must be conducted with real users. | 6 |

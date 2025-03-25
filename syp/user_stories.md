# AiKita User Stories

## User Focus
| ID        | Prio | Epic | User Story                                                                                      | COS (Criteria of Satisfaction)                                                                                   | Effort |
|-----------|------|------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------|
| aikUs01   | 1    | UI/UX | As a teacher, I want a clean and intuitive user interface, so I can easily use the application. | The user interface is user-friendly and easy to learn.                              | 5      |
| aikUs02   | 1    | Child Management | As a teacher, I want to manage child information (add, edit, delete) so I can keep the class list accurate. | I can add, edit, and remove child data easily. | 2      |
| aikUs03   | 2    | Feedback | As a teacher, I want to provide feedback on the application, so it can be improved. | I can submit feedback on the application. | 8 |
| aikUs04   | 1    | Child Management | As a teacher, I want to search for a child by name or ID, so I can quickly find their details. | Search functionality should return accurate results based on name or ID. | 3 |

---

## MVP
| ID        | Prio | Epic | User Story                                                                                      | COS (Criteria of Satisfaction)                                                                                   | Effort |
|-----------|------|------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------|
| aikMvp01a | 1    | UI/UX | As a user I want to launch the app and see a clean welcome screen so I know the app is working. | Tauri shell must start and load Angular UI within 3s. Page should contain app title and a short description. | 1      |
| aikMvp01b | 1    | Forms | As a user, I want a well-structured form with validation so I can enter correct data without errors. | Angular form must include inputs for name, email, phone, etc., with validation and error messages. | 2      |
| aikMvp02a | 1    | Data Processing | As a user I want to submit my form and receive back anonymized data so I can review the result. | A .NET endpoint must accept valid form data and return a JSON object with anonymized fields. Response time must be <1s. | 3      |
| aikMvp02b | 2    | Data Processing | As a developer I want to apply different anonymization strategies depending on field type. | Email must be hashed, names replaced with initials, and phone numbers masked (e.g. ***-1234). | 2      |
| aikMvp03a | 1    | Data Management | As a user, I want to save anonymized data and view stored entries so I can manage my records. | Submitting a valid form saves the anonymized object via EF Core to SQLite, and I can see a list of stored records. | 3      |
| aikMvp04a | 2    | Export | As a user I want to select a record and export it to JSON so I can use it elsewhere. | JSON download must trigger when I click "Export", and downloaded file must match the saved data structure. | 2      |
| aikMvp04b | 3    | Export | As a user I want to export multiple records at once. | A checkbox UI allows selecting multiple entries and saving them to a single JSON array. | 2      |

---

## MVP+ (Core System)
| ID        | Prio | Epic | User Story                                                                                      | COS (Criteria of Satisfaction)                                                                                   | Effort |
|-----------|------|------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------|
| aikCore01 | 1    | Dashboard | As an admin I want to view submitted entries in a clean dashboard so I can review stored data quickly. | Angular-based admin UI must list all entries with filtering and sorting by date. Data must be read from local or cloud backend. | 5 |
| aikCore02 | 2    | Sync | As a user, I want to sync my data to a remote endpoint and track sync events so I can back up my data and monitor sync success. | The .NET backend must accept JSON POST requests, store them in PostgreSQL, and log sync events. | 5 |
| aikCore03 | 2    | Data Management | As a user I want to delete stored records locally so I can manage outdated or incorrect data. | Each entry must have a delete action. Deletion must trigger a confirmation dialog and complete in under 1s. | 2 |
| aikCore04 | 3    | UI/UX | As a user I want to be warned before closing the app with unsaved data so I don’t lose progress. | App must prompt a confirmation dialog when unsaved changes exist in form and window/tab is closed. | 2 |
| aikCore05 | 2    | Dashboard        | As a user, I want to see recent activity in a sidebar so I can quickly check my recent interactions. | A sidebar must display the most recent activities, like data submissions and edits. | 4 |

---

## Data Management & Reports  
| ID        | Prio | Epic | User Story                                                                                      | COS (Criteria of Satisfaction)                                                                                  | Effort |
|-----------|------|------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------|
| aikData01 | 2    | Child Management | As a teacher, I want to manage child lists, so I can organize my classes. | I can create, edit, and delete child lists. | 3 |
| aikData02 | 3    | Progress Tracking | As a teacher, I want to record, review, and track a child's progress over time so I can monitor their development. | I can enter, filter, and review child observations, and display a child's history. | 3 |
| aikData03 | 4    | Reports | As a teacher, I want to export child data into a table, so I can generate reports and share them. | I can export child data in a common table format. | 8 |
| aikData04 | 4    | Reports | As a teacher, I want to generate visual reports and charts, so I can better understand a child's performance. | I can generate charts and graphs that illustrate a child's performance. | 8 |
| aikData05 | 3    | Progress Tracking  | As a teacher, I want to set reminders for tracking progress, so I can ensure timely updates for each student. | Reminders can be set to alert teachers to update or review progress for specific children. | 4 |

---

## Security & Validation
| ID        | Prio | Epic | User Story                                                                                      | COS (Criteria of Satisfaction)                                                                                  | Effort |
|-----------|------|------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------|
| aikSec01  | 1    | Security | As a user, I want my sensitive data to be encrypted both locally and on the client-side so my information remains secure. | DB must use field-level AES encryption or encrypted SQLite file via SQLCipher (or equivalent). | 4 |
| aikSec02  | 2    | Security | As a user, I want to anonymize or exclude sensitive data before exporting or sending it to a server so my privacy is protected. | Export must support an optional flag to include/exclude personal fields. Default: anonymized only. | 3 |
| aikSec03  | 2    | Security | As a user I want all file uploads to be validated to avoid sending invalid or dangerous data to the system. | All JSON must be schema-validated before being processed. Invalid formats must be rejected with errors. | 3 |
| aikSec04  | 2    | Security        | As an admin, I want to be able to audit data access logs, so I can ensure compliance with privacy regulations. | Audit logs must record detailed information on user access and modifications. | 4 |

---

## Cloud API + Admin
| ID        | Prio | Epic | User Story                                                                                      | COS (Criteria of Satisfaction)                                                                                  | Effort |
|-----------|------|------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------|
| aikCloud01 | 2   | API | As a user I want to log in to the cloud API with a token so my syncs are authenticated. | Auth must use simple token auth (e.g., JWT or static) for cloud sync endpoints. Token must be validated server-side. | 3 |
| aikCloud02 | 2   | API            | As an admin, I want to manage cloud-based user permissions, so I can control access to sensitive data. | Admin UI should allow role-based access control for different user groups. | 4 |
| aikCloud03 | 1   | API            | As a user, I want to access cloud-stored data securely, so I can trust that my information is safe. | Cloud API must implement secure protocols like HTTPS and data encryption. | 4 |



---

## Quality Assurance & Performance
| ID      | Prio | Epic | User Story                                                                                      | COS (Criteria of Satisfaction)                                                                                 | Effort |
|--------|------|------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------|
| eduQA01 | 2   | QA | As a QA engineer, I want to write automated tests, so the application is thoroughly tested. | The application is extensively tested and bug-free. | 13 |
| eduQA02 | 1   | QA   | As a QA engineer, I want to use performance testing tools, so I can ensure the application scales under load. | Performance tests should simulate high traffic and ensure the system responds in under 2 seconds. | 12 |
| eduQA03 | 3   | QA   | As a QA engineer, I want to conduct usability testing, so the application is easy to use for all users. | Usability testing sessions should gather feedback from actual users and improve UI/UX. | 6 |

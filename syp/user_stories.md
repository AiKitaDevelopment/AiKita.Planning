### User Focus
| ID        | Prio | User Story                                                                                      | COS                                                                                                                                                                       | Effort |
|-----------|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| aikUs01 | 1     | As a teacher, I want a clean and intuitive user interface, so I can easily use the application. | The user interface is user-friendly and easy to learn.  | 5    |
| aikUs02 | 1   | As a teacher, I want to add new children to a class, so I can keep the class list up to date.   | I can add new children to a class.                              | 1      |
| aikUs03 | 1   | As a teacher, I want to edit child information, so I can correct errors.                        | I can edit and save child information.                          | 1   |
| aikUs04 | 1   | As a teacher, I want to provide feedback on the application, so it can be improved.             | I can submit feedback on the application.                       | 8   |


### MVP

| ID        | Prio | User Story                                                                                      | COS                                                                                                                                                                       | Effort |
|-----------|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| aikMvp01a | 1    | As a user I want to launch the app and see a clean welcome screen so I know the app is working. | Tauri shell must start and load Angular UI within 3s. Page should contain app title and a short description.                        | 1      |
| aikMvp01b | 1    | As a user I want a form with labeled fields so I can enter my personal data.                    | Angular form must include inputs for name, email, phone, etc., with placeholders and labels.                                       | 2      |
| aikMvp01c | 1    | As a user I want to be warned if I enter invalid or incomplete data so I can fix mistakes.       | Form must validate fields live and show clear error messages under each field. Form submit must be disabled when invalid.          | 2      |
| aikMvp02a | 1    | As a user I want to submit my form and receive back anonymized data so I can review the result.  | A .NET endpoint must accept valid form data and return a JSON object with anonymized fields. Response time must be <1s.            | 3      |
| aikMvp02b | 2    | As a developer I want to apply different anonymization strategies depending on field type.       | Email must be hashed, names replaced with initials, and phone numbers masked (e.g. ***-1234).                                     | 2      |
| aikMvp03a | 1    | As a user I want to save the anonymized data to a local database so I don’t lose it.             | Submitting a valid form saves the anonymized object via EF Core to SQLite. Save must return confirmation.                          | 2      |
| aikMvp03b | 1    | As a user I want to view a list of my saved entries so I can confirm what’s stored.              | The app must show a list/table of stored records loaded from the local DB.                                                         | 2      |
| aikMvp04a | 2    | As a user I want to select a record and export it to JSON so I can use it elsewhere.             | JSON download must trigger when I click "Export", and downloaded file must match the saved data structure.                         | 2      |
| aikMvp04b | 3    | As a user I want to export multiple records at once.                                              | A checkbox UI allows selecting multiple entries and saving them to a single JSON array.                                            | 2      |


### MVP+ (Core System)

| ID        | Prio | User Story                                                                                     | COS                                                                                                                                              | Effort |
|-----------|------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| aikCore01 | 1    | As an admin I want to view submitted entries in a clean dashboard so I can review stored data quickly. | Angular-based admin UI must list all entries with filtering and sorting by date. Data must be read from local or cloud backend. | 5 |
| aikCore02 | 2    | As a user I want to sync my data to a remote endpoint so I can keep a backup in the cloud. | The .NET backend must accept JSON POST requests and store them in a PostgreSQL DB. Sync must be confirmed or retried on failure. | 5 |
| aikCore03 | 2    | As a user I want to delete stored records locally so I can manage outdated or incorrect data. | Each entry must have a delete action. Deletion must trigger a confirmation dialog and complete in under 1s. | 2 |
| aikCore04 | 2    | As an admin I want to log data sync events so I can track sync success or failures. | Sync events must be stored in a local log or DB table with timestamps, status (success/fail), and reason. | 3 |
| aikCore05 | 3    | As a user I want to be warned before closing the app with unsaved data so I don’t lose progress. | App must prompt a confirmation dialog when unsaved changes exist in form and window/tab is closed. | 2 |

### Data Management & Reports  

| ID        | Prio | User Story                                                                                     | COS                                                                                                                                              | Effort |
|-----------|------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| aikData01 | 2    | As a teacher, I want to manage child lists, so I can organize my classes.                      | I can create, edit, and delete child lists.                      | 3   |
| aikData02 | 4    | As a teacher, I want to record and review observations about children, so I can track their development. | I can enter, filter, and review child observations.              | 3      |
| aikData03 | 3    | As a teacher, I want to see a child's progress over time, so I can monitor their development.  | I can display a child's history.                                 | 3  |
| aikData04 | 4    | As a teacher, I want to export child data into a table, so I can generate reports and share them. | I can export child data in a common table format.               | 8    |
| aikData05 | 4     | As a teacher, I want to generate visual reports and charts, so I can better understand a child's performance. | I can generate charts and graphs that illustrate a child's performance. | 8   |


### AI Integration

| ID        | Prio | User Story                                                                                   | COS                                                                                                                                                     | Effort |
|-----------|------|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|--------|
| aikAI01   | 1    | As a user I want to upload a JSON file to receive a smart response so I can learn something from the data. | UI must allow file upload (max 2MB), validate JSON format, and pass it to the AI endpoint. Error messages must be descriptive. | 3 |
| aikAI02   | 1    | As a user I want the AI to classify or interpret my data so I can get insight or feedback. | A .NET endpoint must call ONNX Runtime with the input, return a prediction or label, and display the result in the UI within 3s. | 5 |
| aikAI03   | 2    | As a user I want to view past AI predictions so I can track changes or verify responses. | Predictions must be stored in the DB with timestamps and linked to original input data. Admin UI must display them in a table or timeline view. | 4 |
| aikAI04   | 3    | As an admin I want to view AI errors in a log so I can debug or improve input handling. | All exceptions during AI inference must be logged locally with timestamps, input summary, and exception type/message. | 3 |

### Security & Validation

| ID        | Prio | User Story                                                                                    | COS                                                                                                                                   | Effort |
|-----------|------|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|--------|
| aikSec01  | 1    | As a user I want my locally stored data to be encrypted so that it's protected even if someone accesses my device. | DB must use field-level AES encryption or encrypted SQLite file via SQLCipher (or equivalent). | 4 |
| aikSec02  | 2    | As a user I want my JSON export to exclude sensitive data unless explicitly selected. | Export must support an optional flag to include/exclude personal fields. Default: anonymized only. | 3 |
| aikSec03  | 2    | As a user I want all file uploads to be validated to avoid sending invalid or dangerous data to the system. | All JSON must be schema-validated before being processed. Invalid formats must be rejected with errors. | 3 |
| aikSec04 | 1    | As a developer, I want to design a modular and scalable architecture, so the application is easy to maintain and extend. | The application is well-structured and easy to maintain. | 5      |
| aikSec05 | 1    | As a database administrator, I want to define a secure and efficient data structure, so child data is stored and retrieved reliably. | The database is well-organized and secure.                      | 5      |
| aikSec06 | 1    | As a developer, I want to implement client-side encryption for sensitive data, so child information is protected. | Sensitive data is encrypted before being stored.                | 5      |
| aikSec07 | 1    | As a developer, I want to anonymize learning data before sending it to the server, so children's privacy is protected. | Learning data is anonymized before transmission.                | 3      |
| aikSec08 | 2    | As a system administrator, I want to implement access controls, so only authorized users can view child data. | Access controls are implemented, ensuring only authorized users can access child data. | 3      |
| aikSec09 | 4     | As a system administrator, I want to generate audit logs, so I can track user activity and ensure data security. | Audit logs are generated and stored.                            | 3      |


### Optional: Cloud API + Admin

| ID        | Prio | User Story                                                                                       | COS                                                                                                                                    | Effort |
|-----------|------|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|--------|
| aikCloud01 | 2    | As a user I want to log in to the cloud API with a token so my syncs are authenticated. | Auth must use simple token auth (e.g., JWT or static) for cloud sync endpoints. Token must be validated server-side. | 3 |
| aikCloud02 | 3    | As an admin I want to view logs or sync history in the admin panel so I can see usage. | Sync log data must be fetched from the backend and presented with filters (date, status, user token). | 3 |

### Performance & Scaling  

| ID        | Priority | User Story                                                                                      | Criteria of Satisfaction (COS)                                     | Effort |
|----------|----------|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------|
| eduPerf01 | 1        | As a developer, I want to optimize database queries, so the application remains performant with large datasets. | The application remains fast and responsive even with large datasets. | 8      |
| eduPerf02 | 2        | As a system administrator, I want to monitor server performance, so I can identify and resolve bottlenecks. | Server performance is monitored and optimized.                   | 8      |
| eduPerf03 | 1        | As a system administrator, I want to implement load balancing, so the application can support many concurrent users. | The application handles high concurrent usage efficiently.       | 5      |


### Quality Assurance & Feedback  

| ID      | Priority | User Story                                                                           | Criteria of Satisfaction (COS)           | Effort |
|--------|----------|-------------------------------------------------------------------------------------|------------------------------------------|--------|
| eduQA01 | 2        | As a QA engineer, I want to write automated tests, so the application is thoroughly tested. | The application is extensively tested and bug-free. | 13     |

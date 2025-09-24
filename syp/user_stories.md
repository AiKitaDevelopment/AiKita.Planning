 # AiKita User Stories

## User Focus
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikUs01 | 1    | UI/UX            | As a user, I want to navigate the app via a menu, so I can quickly switch between sections. | Menu displays links for planning, childlist and logs correctly. Navigation to these sites works. | 13 | 20 | 75% | |
| aikUs02 | 3    | UI/UX            | As a user, I want to log in, so I can access the content. | Login works, user is redirected to the dashboard. | 8 | 6,5 | 75% | |
| aikUs03 | 3    | UI/UX            | As a user, I want to log out, so my data remains secure. | Logout works, user is redirected to the login page. | 8 | 6,5 | 75% | |
| aikUs03 | 4    | UI/UX            | As a user, I want to see a list of all children in my group, so I can quickly access their information.| Child list is displayed correctly.. | 8 | | | |


---

## MVP
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikMvp01 | 1  | UI/UX            | As a user, I want to launch the app and see a clear welcome screen, so I know it is working. | Tauri shell must load Angular UI within 3s and display app title with a description. | 3 | | | |
| aikMvp02 | 1  | Forms            | As a user, I want structured forms with validation, so I can enter correct data without errors. | Forms must include validation for all fields and display clear error messages. | 2 | | | |
| aikMvp03 | 1  | Data Processing  | As a user, I want to submit a form and receive anonymized data as a backup so I can review and store it securely. | A .NET endpoint must return anonymized JSON data (e.g., hashed emails, masked phone numbers) within 1s. | 5 | | | |
| aikMvp06 | 1  | Data Management  | As a user, I want to save and view anonymized data, so I can manage records efficiently. | Data should be saved via EF Core to SQLite, with a UI list for browsing entries. | 3 | | | |
| aikMvp07 | 2  | Export           | As a user, I want to export selected records, so I can use them externally. | A Download button must export the selected entries in a structured format. | 2 | | | |
| aikMvp08 | 3  | Export           | As a user, I want to export multiple records at once. | A checkbox UI must allow selecting multiple records for batch export. | 2 | | | |

---

## Core System (MVP+)
| ID        | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikCore01 | 1   | Dashboard        | As an admin, I want to view all submitted entries in a structured dashboard. | The admin UI must display stored entries with filtering, sorting, and pagination. | 5 | 10 | 30% | |
| aikCore04 | 2   | UI/UX            | As a user, I want a warning before closing the app with unsaved changes. | The app must show a confirmation dialog when unsaved changes exist. | 2 | | | |
| aikCore05 | 4   | Dashboard        | As a user, I want to see my recent activity in a sidebar. | A sidebar must show a log of recent interactions (e.g., submissions, edits). | 5 | | | |
| aikCore06 | 4  | Dashboard      | As an admin, I want an overview over database interactions in graphs | Amount of visitors, new entries, most popular entries etc must be visualized by easily readable graphs. | 13 | 5 | 10% | |

---

## Data Management & Reports  
| ID        | Prio | Epic               | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|--------------------|-------------|---------------------------------|--------|------|--------|-------|
| aikData03 | 4   | Reports            | As a user, I want to export child data into tables. | I can generate and download CSV or Excel files. | 2 | | | |
| aikData04 | 4   | Reports            | As a user, I want to visualize child performance. | The system must generate charts and graphs from stored data. | 8 | | | |

---

## Security & Validation
| ID        | Prio | Epic     | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|---------|-------------|---------------------------------|--------|-------|--------|-------|
| aikSec01  | 1    | Security | As a user, I want all sensitive data to be encrypted. | AES-256 encryption must be applied. | 21 | | | |
| aikSec02  | 2    | Security | As a user, I want to anonymize or exclude personal data when exporting. | An option must allow exporting anonymized or full data. | 3 | | | |


---

## Cloud API + Admin
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|-------|-------------|---------------------------------|--------|------|--------|-------|
| aikCloud02 | 2   | API   | As a user, I want to log in securely to the child managment system. | Authentication must use JWT with a refresh mechanism. | 3 | | | |
| aikCloud03 | 3   | API   | As an admin, I want role-based user permissions. | The admin UI must allow assigning and modifying roles. | 13 | 8 | 5% | |
| aikCloud04 | 3   | API   | As a user, I want my cloud data to be secure. | The API must enforce HTTPS and encrypt stored data. | 8 | | | |



## Data Vizualisation & Insights
| ID   | Prio | Epic                     | User Story                                                                                              | COS (Criteria of Satisfaction)                                      | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| vi02 | 1    | Visualization & Insights | As a Data Scientist, I want to visually explore vectors and the dataset, so I can detect data patterns. | Clustering/dimensionality reduction (e.g., PCA/TSNE) is visualized. | 4      | 14   | 0%     |   Rio    |



## LLM 
| ID   | Prio | Epic               | User Story                                                                                                | COS (Criteria of Satisfaction)                    | Effort | Time | Status | Owner |
| ---- | ---- | ------------------ | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ------ | ---- | ------ | ----- |
| LLM01 | 2    | Ai predictions | As a user, I want AI-based suggestions for observations, so I can get guidance on activities and developmental categorization. | Suggestions for activity and categorization (area, sub-area, section and goal) are generated by AI. | 3 | 4 | | Mann |
| LLM02 | 2    | ai result analisys | As a user, I want to edit all AI-based suggestions before saving, so the data reflects my judgment. | Users can modify all AI-generated suggestions before saving. | 3 | 4 | | Huber|

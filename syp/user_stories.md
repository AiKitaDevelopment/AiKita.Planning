 # AiKita User Stories

## User Focus
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikUs01 | 1    | UI/UX            | As a user, I want to navigate the app via a menu, so I can quickly switch between sections. | Menu displays links for planning, childlist and logs correctly. Navigation to these sites works. | 13 | 20 | 75% | Huber |
| aikUs02 | 3    | UI/UX            | As a user, I want to log in, so I can access the content. | Login works, user is redirected to the dashboard. | 8 | 6,5 | 75% | Huber |
| aikUs03 | 3    | UI/UX            | As a user, I want to log out, so my data remains secure. | Logout works, user is redirected to the login page. | 8 | 6,5 | 75% | Huber |
| aikUs04 | 4    | UI/UX            | As a user, I want be sure that closing a tab in the browser, logs me out. | SessionStorge was used achieve this. | 8 | 6,5 | 100% | Huber |
| aikUs05 | 4    | UI/UX            | As a user, I want to see a list of all children in my group, so I can quickly access their information.| Child list is displayed correctly. | 8 | 4 | 75% | Huber |
| aikUs06 | 3    | UI/UX            | As a user, I want to see a list of all observations and for one child only as well.| Previous observations are listed. | 8 | 4 | 75% | Huber |


## MVP
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikMvp01 | 1  | UI/UX            | As a user, I want to launch the app and see a clear welcome screen, so I know it is working. | Dashboard must load, after login, within 3s. | 3 | 1 | 100% | Huber |
| aikMvp02 | 1  | Forms            | As a user, I want structured forms with validation, so I can enter correct data without errors. | Core features/forms must include validation for all fields and display clear error messages. | 2 | 6 | 25%| Huber |
| aikMvp07 | 2  | Export           | As a user, I want to export selected records, so I can use them externally. | A Download button must be visible for all records. | 2 | 0 | 0 | Huber |


---

## Core System (MVP+)
| ID        | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikCore06     | 4    | Dashboard       | As an admin, I want an overview over database interactions in graphs                                   | Amount of visitors, new entries, most popular entries etc must be visualized by easily readable graphs.                                                | 13     | 5    | 10%    | Rio   |
| **aikCore07** | 1    | Integration     | As a developer, I want a configured API base and CORS, so the frontend can reach the backend securely. | FE/BE base URL set via environment; CORS allows FE origin; HTTPS-only enforced; `/healthz` reachable; FE connectivity check passes.                    | 3      |      | 0%     |   Rio    |
| **aikCore08** | 1    | Authentication  | As a user, I want login/logout integrated with the backend, so sessions are secure across FE and BE.   | JWT + refresh wired via HTTP interceptor; secure token storage; route guards for protected pages; logout clears session; 2 happy-path E2E tests green. | 5      |      | 0%     |   Rio    |
| **aikCore09** | 2    | Data Management | As a user, I want end-to-end CRUD for children and observations, so I can manage records reliably.     | FE can create/read/update/delete via `/children` & `/observations`; optimistic UI with rollback on error; BE validation messages surfaced in UI.       | 8      |      | 0%     |    Rio   |

---

## Week planner
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikEx01 | 4  | Weekplanner       | A a teacher i want to access my week planner. | Navigation to week planner is implemented and works correctly. | 3 | 5 | 0% | Rio |
| aikEx02 | 4  | Weekplanner       | A a teacher i want to be able to plan my week in a planer. | I can input my planned activities into my week planer. | 5 | 10 | 0% | Rio |
| aikEx03 | 4  | Weekplanner       | A a teacher i want to import planned activties to my week planer. | The week plan can import activities from the planning logs off the last two weeks. | 5 | 10 | 0% | Rio |
| aikEx04 | 4  | Weekplanner       | A a teacher i want to export and download my week planer into a pdf file. | The week planer can be downloaded via "download" button and opens the generated pdf file. | 5 | 10 | 0% | Rio |


---

## Reflection from
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikRef01 | 4  | Reflection form     | A an educator i want to see my reflection form | Reflection form is accessable from menu.| 5 | 10 | 0% | Rio |
| aikRef02 | 4  | Reflection form     | A an educator i want to reflect on my observations in a seperate form. | Input can be saved on reflection form.| 8 | 15 | 0% | Rio |
| aikRef03 | 4  | Reflection form   | A an educator i want to see my weekly recent reflection form upon loading reflection form. | Wekkly Reflection form is automatically loaded. If no input has been made this week, the form is empty. Changes are tracked.| 5 | 10 | 0% | Rio |
| aikRef04 | 4  | Reflection form     | A an educator i want to add my recent observations to my reflection form | Observations can be automatically added to reflection form.| 5 | 10 | 0% | Rio |
| aikRef05 | 4  | Reflection form     | A an educator i want to download my reflection form into a pdf file. | Reflection form can be downloaded via "download" button and opens the generated pdf file. | 5 | 10 | 0% | Rio |

---

## Cloud Api & Admin
| ID         | Prio | Epic | User Story                                                                                                  | COS (Criteria of Satisfaction)                                                                                                                                                                                          | Effort | Time | Status | Owner |
| ---------- | ---- | ---- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| aikCloud05 | 1    | API  | As a developer, I want to provide versioned REST APIs for core entities, so clients can integrate reliably. | OpenAPI 3 spec published; endpoints for auth, children, observations, exports under `/api/v1`; request/response validation; standardized error model; Postman/Insomnia collection available; basic rate-limit in place. | 8      |      | 0%     |   EDIT-Rio    |
| aikCloud06 | 1    | API  | As a devops, I want to deploy the backend to the cloud, so it is accessible and maintainable.               | Docker image build; CI/CD pipeline to staging/prod; health endpoint `/healthz`; logs/metrics available; HTTPS enabled; zero-downtime rolling deploy & documented rollback.                                              | 8      |      | 0%     |   EDIT-Rio    |
| aikCloud07 | 1    | API  | As a devops, I want to run the application database in the cloud, so data is durable and secure.            | Managed DB provisioned; SSL enforced; network access restricted (VPC/IP allowlist); EF Core migrations executed; automated daily backups + retention; credentials stored via secrets manager.                           | 8      |      | 0%     |   EDIT-Rio    |


---


## Security & Validation
| ID        | Prio | Epic     | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|---------|-------------|---------------------------------|--------|-------|--------|-------|
| aikSec01  | 2    | Security | As a user, I want all sensitive data to be encrypted. | AES-256 encryption must be applied. | 21 | | | EDIT-Rio (aufteilen) |
| aikSec99  | 2    | Security | As a developer I want to send authentification data to backend and receive temporary session token. | A valid session token is received by frontend and temporarily stored. | 8 | | | EDIT-Rio (aufteilen) |


---

## Cloud API + Admin
| ID        | Prio | Epic   | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|-------|-------------|---------------------------------|--------|------|--------|-------|
| aikCloud02 | 2   | API   | As a user, I want to log in securely to the child managment system. | Authentication must use JWT with a refresh mechanism. | 3 | | 0% | Rio |
| aikCloud03 | 3   | API   | As an admin, I want role-based user permissions. | The admin UI must allow assigning and modifying roles. | 13 | 8 | 5% | Huber / Rio |
| aikCloud04 | 3   | API   | As a user, I want my cloud data to be secure. | The API must enforce HTTPS and encrypt stored data. | 8 | | |  Rio |



## Data Vizualisation & Insights
| ID   | Prio | Epic                     | User Story                                                                                              | COS (Criteria of Satisfaction)                                      | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| vi02 | 3    | Visualization & Insights | As a Data Scientist, I want to visually explore vectors and the dataset, so I can detect data patterns. | Clustering/dimensionality reduction (e.g., PCA/TSNE) is visualized. | 4      | 14   | 0%     |   Rio    |



## LLM 

| ID    | Prio | Epic               | User Story                                                                                                                                  | COS (Criteria of Satisfaction)                                                                                                                                                 | Effort | Time | Status | Owner |
| ----- | ---- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------ | ---- | ------ | ----- |
| LLM01 | 1    | Result Analysis/UI | As a user, I want to edit all AI-based suggestions before saving, so the data reflects my judgment.                                         | All fields of the AI suggestion are editable in the UI. Changes are saved to DB.                                                                                               | 3      | 0    | 100%     | Huber |
| LLM02 | 1    | Core Pipeline      | As a developer, I want to connect the AI model to the backend, so clients can request predictions.                                          | A REST endpoint `/predict-ziel` is available. It accepts JSON input and returns predictions in agreed DTO.                                                                     | 5      | 12   | 100%   | Mann  |
| LLM03 | 2    | Explainability     | As a user, I want to understand and trust AI results, including why goals were suggested and whether fallback was triggered.                | Response JSON includes confidence, similarity evidence, and `usedFallback`; disclaimer on low-confidence results; Explain panel fields defined; UI badge for fallback planned. | 13     | 15   | 60%    | Mann  |
| LLM04 | 2    | Trust/Reliability  | As a user, I want a result even when the AI is uncertain, so I can continue working without interruption.                                   | If similarity < threshold, LLM fallback is triggered. If LLM unavailable, retrieval-only answer is returned.                                                                   | 2      | 7    | 100%   | Mann  |
| LLM05 | 3    | Evaluation/Logs    | As a developer, I want structured prediction logs, so I can evaluate AI performance later.                                                  | Each request/response pair is appended to `eval_log.jsonl` with trace ID, anonymized inputs, outputs, similarity, thresholds, and decision path; logs are dev-only.            | 3      | 6    | 80%    | Mann  |
| LLM06 | 3    | Performance        | As a user, I want predictions to return quickly, so my workflow is not slowed down.                                                         | 95% of responses under 2s (CPU) and under 5s (GPU fallback). Timeout handling implemented.                                                                                     | 3      | 0    | 0%     | Mann  |
| LLM07 | 2    | Config             | As a developer, I want env-based configuration for endpoints and thresholds, so I can tune providers and behavior without redeploying code. | `LLM_ENDPOINT` loaded from env; `SIM_STRONG`/`SIM_WEAK` thresholds configurable; validation on load; changes take effect after restart.                                        | 5      | 6    | 60%    | Mann  |
| LLM08 | 1    | Core Pipeline      | As a developer, I want an end-to-end SBERT + LLM pipeline, so predictions return 1–3 Ziele reliably.                                        | SBERT embeddings persisted; vector store returns top-k; prompt template stable; LLaMA/Mistral container running; routing via thresholds; JSON validated.                       | 21     | 45   | 100%   | Mann  |
| LLM09 | 1    | Core Pipeline      | As a developer, I want a connected backend with a finalized JSON schema, so services interoperate safely.                                   | `/v1/predict-ziel` returns agreed DTO; error semantics defined; schema validated in Swagger; field names + versioning documented.                                              | 5      | 11   | 100%   | Mann  |
| LLM10 | 2    | Deployment/Ops     | As a developer, I want containerization, controlled access, and documentation, so the service can be deployed and tested safely.            | Draft Dockerfile prepared; ports/env/volumes noted; remote access restricted to ACLs; smoke tests passed; runbook + README updated with pipeline steps and config parameters.  | 8      | 10   | 40%    | Mann  |
| LLM11 | 1    | Core Pipeline      | As a user, I want AI-based suggestions (1–3 Ziele).                                                                                         | End-to-end prediction validated against sample set; acceptance check recorded.                                                                                                 | 2      | 7    | 100%   | Mann  |




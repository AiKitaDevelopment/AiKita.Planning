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

## Cloud Api 
| ID         | Prio | Epic | User Story                                                                                                  | COS (Criteria of Satisfaction)                                                                                                                                                                                          | Effort | Time | Status | Owner |
| ---------- | ---- | ---- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| aikCloud04 | 3   | API   | As a user, I want my cloud data to be secure. | The API must enforce HTTPS and encrypt stored child information. | 13 | 8| 30% |  Rio |
| aikCloud06 | 1    | API  | As a developer, I want to deploy the mvp backend to the cloud, so it is accessible and maintainable.               | Docker image build; CI/CD pipeline to staging/prod; health endpoint `/healthz`; logs/metrics available; HTTPS enabled; zero-downtime rolling deploy & documented rollback.                                              | 13      |   18   | 100%     |   Rio    |
| aikCloud07 | 1    | API  | As a developer, I want to run the application database in the cloud, so data is durable and secure.            | Managed DB provisioned; SSL enforced; EF Core migrations executed;                          | 8      |   10   | 100%     |   Rio    |


---


## Security & Validation
| ID        | Prio | Epic     | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|---------|-------------|---------------------------------|--------|-------|--------|-------|
| aikSec01  | 3    | Security | As a user, I want all sensitive data to be encrypted. | AES-256 encryption must be applied. | 21 | 10 | 10% | Rio |
| aikSec02  | 1    | Security | As a developer I want to send authentification data to backend and receive temporary session token. | A valid session token is received by frontend and temporarily stored. | 8 | 10 | 100% | Rio/Huber |
| aikSec03| 1    | Authentication  | As a user, I want login/logout integrated with the backend, so sessions are secure across FE and BE.   | JWT + refresh wired via HTTP interceptor; secure token storage; route guards for protected pages; logout clears session; | 13     |   14   | 90%     |   Rio / Huber  |
| aikSec05 | 3   | API   | As an admin, I want role-based user permissions. | The admin UI must allow assigning and modifying roles. | 13 | 8 | 5% | Huber / Rio |


---

## Data Vizualisation & Insights
| ID   | Prio | Epic                     | User Story                                                                                              | COS (Criteria of Satisfaction)                                      | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| vi02 | 3    | Visualization & Insights | As a Data Scientist, I want to visually explore vectors and the dataset, so I can detect data patterns. | Clustering/dimensionality reduction (e.g., PCA/TSNE) is visualized. | 4      | 14   | 0%     |   Rio    |
| vi03    | 4    | Dashboard       | As an admin, I want an overview over database interactions in graphs                                   | Amount of visitors, new entries, most popular entries etc must be visualized by easily readable graphs.                                                | 13     | 5    | 10%    | Rio   |

---

## AI Integration

| ID   | Prio | Epic                     | User Story                                                                                              | COS (Criteria of Satisfaction)                                      | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| **aikAi01** | 1    | AI Inference & Persistence | As a user, I want to send data to the AI endpoint `/infer` so I can receive an intelligent recommendation based on input.                       | FE can call `/api/ai/infer` with valid DTO; BE orchestrator processes and validates input; AI orchestration service returns structured result.   | 8      |  10    | 100%     | Rio   |
| **aikAi02** | 1    | AI Inference & Persistence | As a developer, I want an `InferRequestDto` and `InferResponseDto` to transport input/output between FE and BE cleanly.                         | DTOs defined in `AiKita_BE.Common.Contracts.AI`; validation attributes present; serialization tested end-to-end.                                 | 3      |   3   | 100%     | Rio   |
| **aikAi03** | 1    | AI Inference & Persistence | As a backend engineer, I want the `IAiOrchestrator` and `AiOrchestrator` to encapsulate the logic of AI inference calling internal services.    | `AiOrchestrator` implements infer pipeline (input validation → transformation → model call → mapping → return DTO); tested via integration test. | 3      |   2   | 100%     | Rio   |
| **aikAi04** | 1    | AI Inference & Persistence | As a backend engineer, I want `InferService` to manage preprocessing and mapping from entities to AI-ready format.                              | `InferService` converts domain entities → feature vector; reusable across orchestrations; unit tested.                                           | 5      |   4   | 80%     | Rio   |
| **aikAi05** | 1    | AI Inference & Persistence | As a backend engineer, I want the `/save` endpoint to persist the full AI inference result with all relevant metadata.                          | `/api/ai/save` accepts result payload; validation on DTO; stored via `IFullDataWriter`; returns persisted entity id.                             | 8      |   10   | 90%     | Rio   |
| **aikAi06** | 1    | AI Inference & Persistence | As a developer, I want a `SaveRequestDto` and `SaveResponseDto` that mirror the inference output and support persistence metadata.              | DTOs map one-to-one to database schema entities; serialization/deserialization verified.                                                         | 3      |   1   | 100%     | Rio   |
| **aikAi07** | 1    | AI Inference & Persistence | As a backend engineer, I want `IFullDataWriter` to handle persistence logic for saving AI and user data in a transactional manner.              | Implements `SaveResultAsync()`; atomic write; proper logging and rollback on failure.                                                            | 5      |   6   | 100%     | Rio   |
| **aikAi08** | 1    | AI Inference & Persistence | As a backend engineer, I want structured error handling and validation messages surfaced to the frontend when `/infer` or `/save` fail.         | All exceptions caught centrally; mapped to readable validation errors; UI displays feedback without crash.                                       | 13      |   6   | 60%     | Rio / Huber   |
| **aikAi09** | 2    | AI Mock Integration        | As a frontend developer, I want mock endpoints for `/infer` and `/save` so that I can test UI integration before real AI model connection.      | Mock controller methods return dummy DTOs with realistic structure; feature toggled; available in dev environment.                               | 5      |  6    | 100%     | Rio   |


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




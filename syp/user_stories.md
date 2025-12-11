 # AiKita User Stories

## User Focus
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikUs01 | 1    | UI/UX            | As a user, I want to easily enter my observation for a certain child and get back recommended activities. | User prompt is processed by AI to get back recommendations. | 10 | 20 | 100% | Huber/Rio/Mann |
| aikUs02 | 3    | UI/UX            | As a user, I want to log in, so I can access the content. | Login works, user is redirected to the dashboard. | 8 | 12 | 100% | Huber/Rio |
| aikUs03 | 3    | UI/UX            | As a user, I want to log out, so my data remains secure. | Logout works, user is redirected to the login page. | 4 | 6 | 100% | Huber/Rio |
| aikUs04 | 3    | UI/UX            | As a user, I want to see a list of all children in my group, so I can quickly access their information.| Child list is displayed correctly. | 8 | 10 | 100% | Huber |
| aikUs05 | 3    | UI/UX            | As a user, I want to see a list of previous observations + activtites for a child.| Previous observations + activties are listed when child is selected. | 8 | 10 | 100% | Huber |
| aikUs06 | 3    | UI/UX            | As a user, I want change information given in the Navigation bar.| Settings page let's the user change the navigation bar settings. | 4 | 2 | 100% | Huber |


## MVP
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikMvp01 | 1  | UI/UX            | As a user, I want to be taken to the dashboard after logging in, so I can quickly see what I can do in the application. | After a successful login, the user is automatically redirected to the dashboard. | 3 | 2 | 100% | Huber |
| aikMvp02 | 1  | Forms            | As a user, I want the application to prevent me from entering incorrect data, so I can be sure my input is valid. | All forms include validation for every field, and clear, user-friendly error messages are shown when data is invalid. | 2 | 6 | 100%| Huber |
| aikMvp07 | 2  | Export           | As a user, I want to export child records, so I can use them externally. | A Download button must be visible for child records. | 2 | 4 | 100% | Huber |


---

## Cloud Deployment 
| ID         | Prio | Epic | User Story                                                                                                  | COS (Criteria of Satisfaction)                                                                                                                                                                                          | Effort | Time | Status | Owner |
| ---------- | ---- | ---- | ----------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| aikCloud04 | 3   | API   | As a user, I want my cloud data to be secure. | The API must enforce HTTPS and encrypt stored child information. SSL enforced; Encryption for loggin data and sensitive data is ensured. | 13 | 40| 100% |  Rio |
| aikCloud06 | 1    | API  | As a user I want my input data to be accessible from anywhere.            | Database can be accessed via cloud. Data is managed, synchronized regularly and veted for ideal data persistance.                                           | 21     |   40   | 100%     |   Rio    |
| aikCloud07 | 2 | Data Sync | As a user, I want my data to sync automatically with the cloud so my changes are safely stored. | Data is stored in a PostgreSQL database; sync events are logged for reliability. | 13 | 20 | 100% | Rio |
| aikCloud08 | 2 | Data Management | As a user, I want to delete saved records so I can remove outdated or incorrect data. | Each entry has a delete button with a confirmation prompt. | 8 | 5 | 100% | Rio/Huber |
| aikCloud09 | 2    | Core Pipeline      | As a user, I want to access the AiKita app from any computer via a web browser, so I am not tied to a single machine.   |  The full application stack is deployed to Google Cloud Run. The frontend is accessible via a public HTTPS URL and all internal services communicate. The live system passes the 20-sample acceptance test.     | 13      | 25    | 100%   | Huber/Mann/Rio |

---


## Security & Validation
| ID        | Prio | Epic     | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|-----------|------|---------|-------------|---------------------------------|--------|-------|--------|-------|
| aikSec01 | 2 | File Security | As a user, I want uploaded files to be verified so only valid and safe files are processed. | JSON uploads are validated against a schema before processing. | 8 | 2 | 10% | Rio/Huber |
| aikSec02 | 2 | Security & Logging | As a user, I want the system to record all data access so activity can be audited when necessary. | All read/write actions are logged for compliance and traceability. | 8 | 10 | 100% | Rio/Huber |
| aikSec05 | 3   | API   | As a user I want my input data to only be visible by me or my supervisors.| The admin UI must allow assigning and modifying roles. Data access is modified by role based permissions. | 21 | 8 | 20% | Huber / Rio |


---

## Data Vizualisation & Insights
| ID   | Prio | Epic                     | User Story                                                                                              | COS (Criteria of Satisfaction)                                      | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| aikVis01 | 3 | Dashboard & Insights | As a user, I want to see system and data activity in clear graphs so I can identify who accessed what sensitive information. | Visitor counts, new entries, and popular actions are shown in readable charts; PCA/TSNE visualizations included. | 17 | 19 | 50% | Rio/Huber |
| vi03    | 3    | Dashboard       | As a user I want an overview of my recent activities and see statistics on my recent planning Data to detect early imbalances in my planning activity focus.  | Recent activity can be seen in my logs. Planned activity areas must be visualized by easily readable graphs.          | 13     | 5    | 30%    | Rio/Huber   |


---

## AI Integration

| ID   | Prio | Epic                     | User Story                                                                                              | COS (Criteria of Satisfaction)                                      | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| **aikAi01** | 1    | AI Inference & Persistence | As a user, I want to send my observation to the AI, so I can receive an intelligent recommendation based on input.                       | FE can call `/api/ai/infer` with valid DTO; BE orchestrator processes and validates input; AI orchestration service returns structured result.   | 21      |  40    | 100%     | Rio/Huber/Mann   |
| **aikAi04** | 1    | AI Inference & Persistence | As a user I want to receive structured Ai recommendations in the responding fields so i can work with the result. | 'Infer Response' contains all the relevant fields for a full planning set, such as area, subsection, goal, recommendations for activities.   | 13      |   28   | 100%     | Rio/Huber/Mann   |
| **aikAi05** | 1    | AI Inference & Persistence | As a user I want to be able to modify AI recommendations to my needs. |  `/api/ai/save` logs result to database. Ai Model use is logged; validation on DTO;     | 8      |   14   | 100%     | Rio/Huber   |
| **aikAi06** | 1    | AI Inference & Persistence | As a user I want to be able to see and / or modifiy my past planning data.   |  stored via `IFullDataWriter`; returns persisted entity id. Log data is allocated to role. Logdata can be loaded and modified via logs in the ui.   | 21     |   14   | 50%     | Rio/Huber   |
| **aikAi07** | 1    | AI Inference & Persistence | As a user I want to see if AI requests are possible at the moment. I want to know if my UI is connected to the AiModel.    | AI connection healt endpoint is implemented on backend and Ai Model.  Connection is tested via health endpoint. Connection details are forwarded to FE and displayed via symbol on UI.    | 13      |   32   | 100%     | Rio / Huber / Mann   |
| **aikAi08** | 1    | AI Inference & Persistence | As a user I want info texts if something went wrong with my AI requests.    | All exceptions caught centrally; mapped to readable validation errors; UI displays feedback without crash.     | 13      |   6   | 30%     | Rio / Huber / Mann   |


## LLM 

| ID    | Prio | Epic               | User Story                                                                                                                                  | COS (Criteria of Satisfaction)                                                                                                                                                 | Effort | Time | Status | Owner |
| ----- | ---- | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------ | ---- | ------ | ----- |
| LLM01 | 1    | Result Analysis/UI | As a user, I want to edit all AI-based suggestions before saving, so the data reflects my judgment.                                         | All fields of the AI suggestion are editable in the UI. Changes are saved to DB.                                                                                               | 3      | 5    | 100%     | Huber |
| LLM02 | 1    | Core Pipeline      | As a user, I want the system to provide an AI-powered suggestion feature, so I can get help analyzing my observations.                                          | A REST endpoint `/predict-ziel` is available. It accepts JSON input and returns predictions in agreed DTO.                                                                     | 5      | 12   | 100%   | Mann  |
| LLM03 | 2    | Explainability     | As a user, I want to understand and trust AI results, including why goals were suggested and whether fallback was triggered.                | Response JSON includes confidence, similarity evidence, and `usedFallback`; disclaimer on low-confidence results; Explain panel fields defined; UI badge for fallback planned. | 13     | 15   | 60%    | Mann  |
| LLM04 | 2    | Trust/Reliability  | As a user, I want a result even when the AI is uncertain, so I can continue working without interruption.                                   | If similarity < threshold, LLM fallback is triggered. If LLM unavailable, retrieval-only answer is returned.                                                                   | 2      | 7    | 100%   | Mann  |
| LLM05 | 3    | Evaluation/Logs    | As a project administrator, I want structured prediction logs, so I can evaluate AI performance later.                                                  | Each request/response pair is appended to `eval_log.jsonl` with trace ID, anonymized inputs, outputs, similarity, thresholds, and decision path; logs are dev-only.            | 3      | 6    | 80%    | Mann  |
| LLM06 | 3    | Performance        | As a user, I want predictions to return quickly, so my workflow is not slowed down.                                                         | 95% of responses under 2s (CPU) and under 5s (GPU fallback). Timeout handling implemented.                                                                                     | 3      | 0    | 0%     | Mann  |
| LLM07 | 2    | Config             | As a user, I want the AI's sensitivity to be easily adjustable, so its behavior can be fine-tuned based on preference. | `LLM_ENDPOINT` loaded from env; `SIM_STRONG`/`SIM_WEAK` thresholds configurable; validation on load; changes take effect after restart.                                        | 5      | 6    | 60%    | Huber/Mann  |
| LLM08 | 1    | Core Pipeline      | As a user, I want the AI to suggest goals that are directly related to my observation notes, so I can save time searching for the right educational focus.     | A pre-defined test set of 20 sample observations is created. The AI must return a relevant and appropriate goal for at least 15 of the 20 (75%) samples, as judged by the project team. The system must reliably return 1-3 suggestions for each valid input.         | 21     | 45   | 100%   | Mann  |
| LLM09 | 1    | Core Pipeline      | As a user, I want the AI suggestion feature to work reliably without data-related crashes, so I can use the tool without interruption.                                   | `/v1/predict-ziel` returns agreed DTO; error semantics defined; schema validated in Swagger; field names + versioning documented.                                              | 5      | 11   | 100%   | Mann  |
| LLM10 | 2    | Deployment/Ops     | As a project administrator, I want the entire application (FE, BE, AI, LLM) to be fully containerized and orchestrated, so the full stack can be reliably run in any environment with a single command.            | All four services are defined in docker-compose.yml. All services communicate via Docker networking. The frontend URL is dynamically configured at runtime via an entrypoint script. The full stack is 100% functional on a local machine. | 13      | 28   | 100%    | Mann  |
| LLM11 | 1    | Core Pipeline      | As a user, I want AI-based suggestions (1–3 Ziele).                                                                                         | End-to-end prediction validated against sample set; acceptance check recorded.                                                                                                 | 2      | 7    | 100%   | Mann  |
| LLM12 | 1    | Core Pipeline      | As a user, I want to know how accurate the AI rates it's response so I can double check low accuracy results.   |  Precision is displayed with ai response and is logged alongside all saved LogData.      | 13      | 13    | 7%   | Huber/Mann/Rio |
| LLM13 | 2    | Trust/Reliability      | As a user, I want the AI's suggested goals to be more creative and specific, so the suggestions provide new ideas, not just simple keyword matches.   |  The new prompt logic is implemented. When tested against the 20-sample set, the AI suggestions are judged to be more context-aware and less repetitive than the old prompts.     | 21      | 0    | 0%   | Mann/Rio |

---


## Week planner
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikEx01 | 3  | Weekplanner       | A a user i want to access my week planner. | Navigation to week planner is implemented and works correctly. | 3 | 5 | 100% | Rio |
| aikEx02 | 3  | Weekplanner       | A a user i want to be able to plan my week in a planer. | I can input my planned activities into my week planer. | 5 | 15 | 100% | Rio |
| aikEx03 | 3  | Weekplanner       | A a user i want to import planned activties to my week planer. | The week plan can import activities from the planning logs off the last two weeks. | 5 | 6 | 100% | Rio |
| aikEx04 | 3  | Weekplanner       | A a user i want to export and download my week planer into a pdf file. | The week planer can be downloaded via "download" button and opens the generated pdf file. | 5 | 10 | 0% | Rio |


---

## Reflection from
| ID      | Prio | Epic            | User Story  | COS (Criteria of Satisfaction)  | Effort | Time | Status | Owner |
|---------|------|-----------------|-------------|---------------------------------|--------|------|--------|-------|
| aikRef01 | 3  | Reflection form     | A a user i want to see my reflection form | Reflection form is accessable from menu.| 5 | 10 | 0% | Rio |
| aikRef02 | 3  | Reflection form     | A a user i want to reflect on my observations in a seperate form. | Input can be saved on reflection form.| 8 | 15 | 0% | Rio |
| aikRef03 | 3  | Reflection form   | A a user i want to see my weekly recent reflection form upon loading reflection form. | Wekkly Reflection form is automatically loaded. If no input has been made this week, the form is empty. Changes are tracked.| 5 | 10 | 0% | Rio |
| aikRef04 | 3  | Reflection form     | A a user i want to add my recent observations to my reflection form | Observations can be automatically added to reflection form.| 5 | 10 | 0% | Rio |
| aikRef05 | 3  | Reflection form     | A a user i want to download my reflection form into a pdf file. | Reflection form can be downloaded via "download" button and opens the generated pdf file. | 5 | 10 | 0% | Rio |

---

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


## Data Preparation & Data quality
| ID   | Prio | Epic                       | User Story                                                                                                                               | COS (Criteria of Satisfaction)                                     | Effort | Time | Status | Owner |
| ---- | ---- | -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ | ------ | ---- | ------ | ----- |
| dq00 | 1    | Data Preparation & Quality | As a data scientist, I want to clean and preprocess raw text data using stemming and regex so that the model can work with consistent input.| Preprocessed text is prepared for model training in the correct format. Stopwords, special chars, and noise are removed properly. | 3      | 8    | 100%     |   Rio    |
| dq01 | 1    | Data Preparation & Quality | As a Data Scientist, I want to merge CSV files from different developmental areas, so I have a unified training dataset.                 | All data sources are merged and validated correctly.               | 3      | 8    | 100%     |   Rio    |
| dq02 | 1    | Data Preparation & Quality | As a Data Scientist, I want to check the structure and number of columns in input files, so data consistency is ensured.                 | Files with mismatched structure are detected and logged.           | 1      | 3    | 100%     |   Rio    |
| dq03 | 1    | Data Preparation & Quality | As a Data Scientist, I want to preprocess texts, so noise in the data is reduced.                                                        | Clean and standardized text is available in the dataset. Text is preprocessed and tokenized in preparation for model training.           | 3      | 8    | 100%     |    Rio   |
| dq04 | 1    | Data Preparation & Quality | As a Data Scientist, I want to transform labels into multi-label format, so multiple assignments per observation are captured correctly. | Labels are available as multi-label binarization. Sclearn multilabling algorithm is used.                  | 2      | 5    | 100%     |    Rio   |
| dq05 | 1    | Data Preparation & Quality | As a Data Scientist, I want to iteratively clean data whenever the AI reveals weaknesses, so dataset quality improves continuously.      | Iterative cleaning is documented and integrated into the workflow. |  13    | 30   | 100%     |   Rio    |

## ML Model Training and Features
| ID   | Prio | Epic                      | User Story                                                                                                               | COS (Criteria of Satisfaction)                             | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------- | ------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------- | ------ | ---- | ------ | ----- |
| mf01 | 1    | Model Training & Features | As a Data Scientist, I want to convert observations into Sentence-BERT vectors, so semantic similarities are captured and word positioning is taken into consideration.   | SBERT vectors are available for training and evaluation.   | 5      | 10   | 100%     |    Rio   |
| mf02 | 1    | Model Training & Features | As a Data Scientist, I want to store vectors in Atlas MongoDB, so I can reuse them later.                                | Vectors can be stored and retrieved from MongoDB.          | 3      | 6   | 100%     |   Rio    |
| mf03 | 1    | Model Training & Features | As a Data Scientist, I want to train a multi-label model, so observations can belong to multiple developmental areas.    | Model is trained successfully. Most likely Areas are logged in descending order of likelyhood. . | 4      | 10   | 100%     |   Rio    |
| mf04 | 1    | Model Training & Features | As a Data Scientist, I want to test different thresholds, so I can find the best trade-off between precision and recall. | Threshold evaluation with comparison plots is available.   | 5      | 12    | 100%     |    Rio   |
| mf05 | 1    | Model Training & Features | As a Data Scientist, I want to implement variable clustering sizes to optimize my sorting accuracy while keeping an acceptable degree of sepcialization.       | Amount of clusters can be manually controlled. Accuracy is logged. | 4      | 12   | 100%     |    Rio   |
| mf06 | 1    | Model Training & Features | As a Data Scientist, I want to implement TF-IDF features for subsections, so specific terms get stronger weights.        | TF-IDF features are integrated into the training pipeline. | 4      | 12   | 100%     |    Rio   |


## ML Model Evaluation & Analysis
| ID   | Prio | Epic                  | User Story                                                                                                                       | COS (Criteria of Satisfaction)                                    | Effort | Time | Status | Owner |
| ---- | ---- | --------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| ea01 | 1    | Evaluation & Analysis | As a Data Scientist, I want to generate classification reports, so I can measure model quality per label.                        | Reports with precision, recall, F1-score per class are available. | 2      | 6    | 100%     |    Rio   |
| ea02 | 1    | Evaluation & Analysis | As a Data Scientist, I want to calculate and save confusion matrices, so misclassifications are visible.                         | Multi-label confusion matrix is available as CSV/plot.            | 3      | 8    | 100%     |    Rio   |
| ea03 | 1    | Evaluation & Analysis | As a Data Scientist, I want to log misclassified observations in a CSV, so I can analyze weaknesses.                             | CSV with misclassification examples is generated.                 | 3      | 8    | 100%     |    Rio   |
| ea04 | 1    | Evaluation & Analysis | As a Data Scientist, I want to output the most common words and top words per class, so I can identify linguistic patterns.      | Word frequency lists are available in reports/logs for TF-idf models with single labeling algorithm.               | 2      | 5    | 100%     |    Rio   |
| ea05 | 1    | Evaluation & Analysis | As a Data Scientist, I want to visualize precision-recall curves per class for multilabeling algorithms, so I can understand variations in model performance. | PR curves per ml models with sclearn algorithm are plotted.                                  | 3      | 10   | 100%     |    Rio   |


## Data Vizualisation & Insights
| ID   | Prio | Epic                     | User Story                                                                                              | COS (Criteria of Satisfaction)                                      | Effort | Time | Status | Owner |
| ---- | ---- | ------------------------ | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------ | ---- | ------ | ----- |
| vi01 | 1    | Visualization & Insights | As a Data Scientist, I want to visualize label distribution, so I can detect imbalanced datasets early. | Bar chart with label support is available.                          | 2      | 6    | 100%     |   Rio    |
| vi02 | 1    | Visualization & Insights | As a Data Scientist, I want to visually explore vectors and the dataset, so I can detect data patterns. | Clustering/dimensionality reduction (e.g., PCA/TSNE) is visualized. | 4      | 14   | 0%     |   Rio    |


## Deployment & Reuse
| ID   | Prio | Epic               | User Story                                                                                                | COS (Criteria of Satisfaction)                    | Effort | Time | Status | Owner |
| ---- | ---- | ------------------ | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ------ | ---- | ------ | ----- |
| dw01 | 1    | Deployment & Reuse | As a Data Scientist, I want to save the trained model and the label binarizer, so I can reuse them later. | Model files are stored as `.pkl` and versioned.   | 2      | 6    | 100%     |    Rio   |
| dw02 | 1    | Deployment & Reuse | As a Developer, I want to load saved models and vectorizers, so I can run predictions in production.      | Loading and prediction on new observations works. | 3      | 8    | 0%     |    Rio   |


## LLM 
| ID   | Prio | Epic               | User Story                                                                                                | COS (Criteria of Satisfaction)                    | Effort | Time | Status | Owner |
| ---- | ---- | ------------------ | --------------------------------------------------------------------------------------------------------- | ------------------------------------------------- | ------ | ---- | ------ | ----- |
| LLM01 | 2    | Ai predictions | As a user, I want AI-based suggestions for observations, so I can get guidance on activities and developmental categorization. | Suggestions for activity and categorization (area, sub-area, section and goal) are generated by AI. | 3 | 4 | | Mann |
| LLM02 | 2    | ai result analisys | As a user, I want to edit all AI-based suggestions before saving, so the data reflects my judgment. | Users can modify all AI-generated suggestions before saving. | 3 | 4 | | Huber|

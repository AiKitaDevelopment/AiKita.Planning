## Summary

|Calculation Set|Included Stories|Completed Effort|Projected Time (hrs)|Velocity (hrs/effort)|
|---|---|---|---|---|
|**Velocity 1** (All)|Planning + All others|55.2|371.67|**6.73**|
|**Velocity 2** (Non-Plan)|Only implementation stories|50.2|342.67|**6.83**|


Exclude outliers:

- `aikSec01` - Effort 21 (est. 120hrs)
    
Recalculated total (without outliers):

|Metric|Value|
|---|---|
|Adjusted Completed Effort|50.2 - (0.65 + 1.5) = **48.05**|
|Adjusted Time|342.67 - (160 + 33.33) = **149.34**|
|**New Avg Velocity**|149.34 ÷ 48.05 = **3.11 hrs/effort** ✅|

---
## All Stories (Planning + Others)

- **Projected Total Time** = actual_time ÷ completion
- **Completed Effort** = effort × completion
- **Velocity** = projected_total_time ÷ effort (not scaled)

| Story      | Effort | Time | Completion | Completed Effort | Projected Time | Velocity (h/effort)     |
| ---------- | ------ | ---- | ---------- | ---------------- | -------------- | ----------------------- |
| aikPlan01  | 3      | 13   | 100%       | 3.00             | 13             | 4.33                    |
| aikPlan01  | 3      | 16   | 100%       | 3.00             | 16             | 5.33                    |
| aikUs01    | 13     | 20   | 75%        | 9.75             | 26.67          | 2.05                    |
| aikUs02    | 8      | 6.5  | 75%        | 6.00             | 8.67           | 1.08                    |
| aikMvp04   | 3      | 2    | 100%       | 3.00             | 2              | 0.67                    |
| aikMvp05   | 3      | 2    | 100%       | 3.00             | 2              | 0.67                    |
| aikCore01  | 5      | 10   | 30%        | 1.50             | 33.33          | 6.67                    |
| aikCore02  | 13     | 20   | 100%       | 13.00            | 20             | 1.54                    |
| aikCore06  | 13     | 5    | 10%        | 1.30             | 50             | 3.85                    |
| aikSec03   | 3      | 20   | 100%       | 3.00             | 20             | 6.67                    |
| aikSec04   | 5      | 10   | 100%       | 5.00             | 10             | 2.00                    |
| aikCloud01 | 3      | 10   | 100%       | 3.00             | 10             | 3.33                    |
| aikCloud03 | 13     | 8    | 5%         | 0.65             | 160            | 12.31                   |
| **Total**  | —      | —    | —          | **55.20**        | **371.67**     | **6.73 h/effort (avg)** |

Velocity = hours/effort ​≈ ==6.73==


---

## All Stories EXCEPT Planning

|Story|Effort|Time|Completion|Completed Effort|Projected Time|Velocity|
|---|---|---|---|---|---|---|
|aikUs01|13|20|75%|9.75|26.67|2.05|
|aikUs02|8|6.5|75%|6.00|8.67|1.08|
|aikMvp04|3|2|100%|3.00|2|0.67|
|aikMvp05|3|2|100%|3.00|2|0.67|
|aikCore01|5|10|30%|1.50|33.33|6.67|
|aikCore02|13|20|100%|13.00|20|1.54|
|aikCore06|13|5|10%|1.30|50|3.85|
|aikSec03|3|20|100%|3.00|20|6.67|
|aikSec04|5|10|100%|5.00|10|2.00|
|aikCloud01|3|10|100%|3.00|10|3.33|
|aikCloud03|13|8|5%|0.65|160|12.31|
|**Total**|—|—|—|**50.20**|**342.67**|**6.83 h/effort (avg)**|

Velocity = hours/effort ​≈ ==6.83==


---


Outliers:

| Story          | Effort | Completion | Time | Projected Time | Velocity (h/effort) |
| -------------- | ------ | ---------- | ---- | -------------- | ------------------- |
| **aikCloud03** | 13     | 5%         | 8    | **160**        | **12.31**           |
| **aikCore01**  | 5      | 30%        | 10   | **33.33**      | **6.67**            |
| **aikSec03**   | 3      | 100%       | 20   | **20**         | **6.67**            |
| aikCore06      | 13     | 10%        | 5    | 50             | 3.85                |
| aikPlan01      | 3      | 100%       | 16   | 16             | 5.33                |
| aikCloud01     | 3      | 100%       | 10   | 10             | 3.33                |
| aikPlan01      | 3      | 100%       | 13   | 13             | 4.33                |
| aikSec04       | 5      | 100%       | 10   | 10             | 2.00                |
| aikUs01        | 13     | 75%        | 20   | 26.67          | 2.05                |
| aikCore02      | 13     | 100%       | 20   | 20             | 1.54                |
| aikUs02        | 8      | 75%        | 6.5  | 8.67           | 1.08                |
| aikMvp04       | 3      | 100%       | 2    | 2              | 0.67                |
| aikMvp05       | 3      | 100%       | 2    | 2              | 0.67                |



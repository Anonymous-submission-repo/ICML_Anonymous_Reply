# ICML_Anonymous_Reply

Thanks for your constructive suggestions and feedback! Please find the additional experimental results and responses below.

## Additioanl Experiments 

### Comparisions with PRMs (Q1)

| **Agentic Systems Types**            | **With Ground Truth** Algorithm Generated | **With Ground Truth** Hand Crafted | **Without Ground Truth** Algorithm Generated | **Without Ground Truth** Hand Crafted |
|-------------------------------------|-----------------------------------------------|-----------------------------------------|---------------------------------------------------|---------------------------------------------|
| All-at-Once Agent-Level Accuracy | **54.33**                                  | **55.17**                                | **51.12**                                         | **53.44**                                    |
| All-at-Once Step-Level Accuracy  | 12.50                                      | 5.26                                     | 13.53                                             | 3.51                                         |
| Step-by-Step Agent-Level Accuracy | 35.20                                     | 34.48                                    | 26.02                                             | 32.75                                        |
| Step-by-Step  Step-Level Accuracy  | **25.51**                                  | **7.02**                                 | 15.31                                             | **8.77**                                     |
| Binary Search Agent-Level Accuracy | 44.13                                    | 51.72                                    | 30.11                                             | 36.21                                        |
| Binary Search Step-Level Accuracy  | 23.98                                     | 6.90                                     | **16.59**                                         | 6.90                                         |
| **Qwen-2.5-MATH-7B-PRM800k** Agent-Level Accuracy | 39.79                                 | 37.93                               | 35.71                                        | 34.48                                    |
| **Qwen-2.5-MATH-7B-PRM800k**  Step-Level Accuracy  | 17.34                                      | 3.45                                     | 14.29                                             | 3.45                                         |
| **Skywork-PRM-7b** Agent-Level Accuracy | 40.81                                    | 32.76                                    | 37.76                                            | 27.59                                        |
| **Skywork-PRM-7b**  Step-Level Accuracy  | 17.34                                 | 5.17                                | 13.27                                             | 1.72                                     |
| **Skywork-PRM-1.5b** Agent-Level Accuracy | 33.67                                    | 29.31                                    | 29.59                                             | 24.14                                        |
| **Skywork-PRM-1.5b** Step-Level Accuracy  | 7.14                                    | 3.45                                     | 7.14                                        | 1.72                                         |


**Caption:** In light of your constructive suggestions, we evaluated the top 3 PRMs in [3] for failure attribution, using the same experimental setting as in Table 1. Specifically, for each agent trajectory, we used the PRM to assign rewards to individual steps, identified the step with the lowest reward, and attributed the decisive error to that step and its corresponding agent. The results are presented above. We observe that none of the PRMs outperform the All-at-Once method in agent-level accuracy, or perform better than the Step-by-Step method in step-level accuracy. Meanwhile, we believe the undesirable performance of PRM methods again indicates the fundamental difference between the task focused by PRM and the task proposed by us. 



### Overlap Percentages of First-Error Step and Decisive-Error Step (Q4)


|                 | Same | Different |
|-----------------|------|-----------|
| The same or Not?|48.21%|   51.79%  |


**Caption:** In light of your suggestions, we conducted an additional round of annotations—using the same guidelines—on the hand-crafted agentic systems to identify the first-error step. We then compared it to the annotated decisive error step and reported the percentage of overlap in the table below. Due to limited rebuttal time, we focused this analysis only on the hand-crafted systems. The results show that in nearly half of the cases, the first error is followed by successful self-correction, and the decisive error step is not the same as the first mistake.  


### Multiple LLM Runs (Q6)


|                      | All-at-Once | Step-by-Step | Binary      |
|----------------------|-------------|--------------|-------------|
| Agent-Level Accuracy | 53.96 (2.7) | 34.65 (2.2)  | 43.27 (3.4) |
| Step-Level Accuracy  | 3.96 (0.4)  | 7.78 (0.8)   | 5.86 (0.7)  |


**Caption:** We conducted five runs for each of the three methods under the same setting as Table 4 and reported the results with standard deviation below. We observe that the conclusions presented in the paper still hold—the relative ranking of the different methods remains consistent across evaluation metrics.


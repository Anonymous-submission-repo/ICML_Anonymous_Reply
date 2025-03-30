# ICML_Anonymous_Reply

Thanks for your constructive suggestions and feedback! The insightful and constructive suggestions have enabled us to effectively improve our work. Please find the additional experimental results and responses below.

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

### Overlap Percentages of First-Error Step and Decisive-Error Step (Q4)


|                 | Same | Different |
|-----------------|------|-----------|
| The same or Not?|48.21%|   51.79%  |





## More Replies

**[6. Were the results averaged over multiple LLM runs? What is the variance?]**

Thanks for the feedback. We do not run multiple LLM trials for three reasons: 

**(1)** the inherent randomness has minimal impact on failure attribution performance, as the task is inherently challenging; 

**(2)** small variations do not affect the main conclusions of the paper—such as the relative ranking of the three attribution methods; and (3) the large computation cost.

However, in light of your suggestions, we conducted five runs for each of the three methods under the same setting as Table 4 and reported the results with variance below. We observe that the conclusions presented in the paper still hold—the relative ranking of the different methods remains consistent across evaluation metrics.


|                      | All-at-Once | Step-by-Step | Binary      |
|----------------------|-------------|--------------|-------------|
| Agent-Level Accuracy | 53.96 (2.7) | 34.65 (2.2)  | 43.27 (3.4) |
| Step-Level Accuracy  | 3.96 (0.4)  | 7.78 (0.8)   | 5.86 (0.7)  |

**[7.  Are the disagreements between annotators usually within a range of steps?]**


Thanks for the feedback. No, disagreements are not necessarily confined to a narrow range of steps. Actually, the ambiguous decisive-error between annotators do not exhibit a strong correlation with their positional distance within the trajectory. 


**[8. Fig. 5 error bars are too large.]**


Thank you for the feedback. We acknowledge that the original figure may be difficult to interpret. In the revised version, we will replace it with a table reporting these results.

**[9. What length values do the 5 levels in Figure 4 correspond to?]**

Thank you for your feedback. The five levels in Figure 4 correspond to different context lengths of agentic system trajectories. Specifically, we evenly divide the range of failure log lengths—from the minimum to the maximum—into five distinct levels, with context lengths progressively increasing from Level 1 to Level 5. The approximate ranges are as follows: Level 1 corresponds to lengths of 5–17 steps, Level 2 to 19–29 steps, Level 3 to 31–49 steps, Level 4 to 51–91 steps, and Level 5 to 93–130 steps. We report both agent-level accuracy and step-level accuracy separately for each level. We will make this clearer in the revised manuscript. Thank you again for your helpful suggestion.

**[10. Lines 036-040 and 047-059 are weirdly phrased?]**

Thank you for the constructive suggestions! In the next version, we will rephrase the sentences to make them clearer. Please let us know if you have any detailed revision suggestions—we’re eager to address them.

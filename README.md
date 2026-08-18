# LLM Response Evaluation & Annotation — AI Trainer Portfolio
Building evaluation datasets to assess LLM response quality based on predefined rubrics, conducting pairwise preference ranking, identifying errors, and performing error analysis.

# Overview
This project evaluates Response A and Response B using the same prompt. Each response is compared based on a predefined evaluation focus, such as factual accuracy, clarity, instruction following, safety, or professionalism.

The goal is to identify which response better satisfies the requirements of each task.

# Dataset
The dataset contains 35 evaluation tasks across multiple categories:
9 General QA	
4 Instruction Following	
8 Summarization	
8 Writing	
2 Hallucination	
1 Fairness	
2 Safety	
1 Privacy	

Each raw data record contains:

task_id — 
category — 
prompt — 
response_a — 
response_b — 

## Repository Structure

```text
llm-evaluation/
├── data/
│   ├── raw/
│   └── processed/
├── results/
│   ├── overall_results.csv
│   └── category_results.csv
└── README.md

## Results
| Response A | 16 | 45.71% |
| Response B | 13 | 37.14% |
| Tie | 6 | 17.14% |

Excluding ties, Response A was preferred in **55.17%** of comparisons, compared with **44.83%** for Response B.

> These results reflect this evaluation set and should not be interpreted as a general measure of model superiority.

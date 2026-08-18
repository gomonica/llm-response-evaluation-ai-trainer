# LLM Response Evaluation & Annotation — AI Trainer Portfolio

Building evaluation datasets to assess LLM response quality using predefined rubrics, pairwise preference ranking, error identification, and error analysis.

## Overview

This project evaluates **Response A** and **Response B** using the same prompt. Each response is compared based on a predefined evaluation focus, such as factual accuracy, clarity, instruction following, safety, or professionalism.

The goal is to identify which response better satisfies the requirements of each task.

## Dataset

The dataset contains **35 evaluation tasks** across multiple categories:

| Category | Tasks |
|---|---:|
| General QA | 9 |
| Instruction Following | 4 |
| Summarization | 8 |
| Writing | 8 |
| Hallucination | 2 |
| Fairness | 1 |
| Safety | 2 |
| Privacy | 1 |
| **Total** | **35** |

Each raw data record contains:

- `task_id` — unique task identifier
- `category` — task category
- `prompt` — input prompt given to both responses
- `response_a` — first model response
- `response_b` — second model response

## Evaluation Methodology

Each response pair is evaluated using a task-specific focus.

Examples include:

- Factual accuracy
- Completeness
- Clarity
- Instruction adherence
- Safety
- Fairness
- Professionalism
- Hallucination
- Privacy

Each task receives one of three preference labels:

- **A** — Response A is better
- **B** — Response B is better
- **Tie** — Both responses are comparable

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
```
```


## Results

| Outcome | Count | Percentage |
|---|---:|---:|
| Response A | 16 | 45.71% |
| Response B | 13 | 37.14% |
| Tie | 6 | 17.14% |
| **Total** | **35** | **100%** |

Excluding ties, Response A was preferred in **55.17%** of comparisons, compared with **44.83%** for Response B.

### Results by Category

| Category | Total | A Wins | B Wins | Ties |
|---|---:|---:|---:|---:|
| General QA | 9 | 7 | 1 | 1 |
| Instruction Following | 4 | 2 | 0 | 2 |
| Summarization | 8 | 2 | 3 | 3 |
| Writing | 8 | 0 | 8 | 0 |
| Hallucination | 2 | 1 | 1 | 0 |
| Fairness | 1 | 1 | 0 | 0 |
| Safety | 2 | 2 | 0 | 0 |
| Privacy | 1 | 1 | 0 | 0 |


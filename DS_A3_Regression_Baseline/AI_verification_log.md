# AI-use and verification log — DS-A3

## AI tool and tasks
I used ChatGPT (OpenAI) as an AI assistant during preparation of the DS-A3 regression assignment. Tasks included clarifying the assignment requirements, reviewing the planned chronological split and leakage safeguards, helping interpret model-comparison and diagnostic outputs, identifying presentation inconsistencies to check, and drafting documentation for reproducibility and the submission summary.

## Advice accepted
- Keep the chronological train/validation/test split fixed and do not use the test set for model selection.
- Report the baseline and candidate-model comparisons, residual diagnostics, influence checks, heteroscedasticity checks, learning curve, and validation error slices.
- Distinguish the primary feature plan (which excludes `yr`) from the separate `yr` sensitivity candidate.
- Discuss negative validation R², diagnostic limitations, and the difference between predictive association and causal evidence.
- Keep environment information, raw result files, reproduction instructions, and a stable versioned repository with the notebook and PDF.

## Advice not treated as a substitute for evidence
AI-generated suggestions and interpretations were not treated as execution results or external evidence. No result was added solely because an AI assistant suggested it. Logistic regression was not treated as interchangeable with linear regression because the target `cnt` is a continuous numeric count; any departure from the literal candidate-family wording should be explained in the notebook rather than hidden.

## Independent verification performed
The notebook was run in Google Colab using the user's reported “Restart session and run all” workflow, and the user reported that it completed without errors. The user also reported checking the final consistency output, including required result-file checks, 110 validation predictions, and confirmation that the test set was not used for model selection. These are user-reported checks; this log does not claim that the AI independently executed the notebook or accessed the user's GitHub account.

## Remaining verification before submission
- Confirm the committed notebook and PDF come from the same final run.
- Confirm all raw files under `data/` and `results/`, the environment lock, and the README are committed.
- Confirm the repository commit/tag is stable and the submitted URL opens without permission problems.
- Confirm the platform summary is 150–300 words.

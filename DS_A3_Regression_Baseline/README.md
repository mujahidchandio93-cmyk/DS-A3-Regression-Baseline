\# DS-A3: Regression Baseline and Diagnostics



\## Research question



How well can interpretable regression baselines predict daily bike-sharing demand (`cnt`) using calendar and weather features, and where do their errors limit the conclusions?



\## Project files



\- `DS\\\\\\\_A3\\\\\\\_Regression\\\\\\\_Baseline.ipynb` — notebook containing the analysis, code, recorded outputs, and diagnostic checks.

\- `DS\\\\\\\_A3\\\\\\\_Regression\\\\\\\_Baseline.pdf` — PDF export of the notebook.

\- `AI\\\\\\\_use\\\\\\\_log.md` — disclosure of AI assistance and verification activities.

\- `RESULT\\\\\\\_SUMMARY.md` — summary prepared for the course submission.

\- `data/day.csv` — daily bike-sharing dataset used in the analysis.

\- `results/` — generated audit files, model comparisons, predictions, diagnostics, and environment information.



Include the `data/` and `results/` files listed above in the repository before submitting.



\## Dataset and provenance



The analysis uses the UCI Bike Sharing daily dataset (`day.csv`). The notebook records the dataset audit and checksum. The dataset should remain unchanged during reproduction; any changes to its source or contents must be documented.



\## Reproduction instructions



1\. Use the Python and package versions recorded in `results/environment\\\\\\\_record.json` and `results/requirements-lock.txt`.

2\. Open the notebook in Jupyter or Google Colab.

3\. Restart the runtime and execute the notebook from top to bottom.

4\. Confirm that all cells complete without errors and that the final consistency checks pass.

5\. Save the executed notebook and export a matching PDF.

6\. Ensure that the notebook, PDF, dataset, generated results, and documentation correspond to the same final analysis.



\## Evaluation design



The dataset is divided chronologically into 511 training observations, 110 validation observations, and 110 test observations. Training data are used for fitting and hyperparameter tuning, while validation data are used for model comparison. The test set must not be used for model selection.



The primary feature plan excludes `yr`. The model including `yr` is reported separately as a sensitivity candidate because its validation performance differs substantially from the primary specification.



\## Results and limitations



The reported Ridge model with `yr` achieved validation MAE of 786.386, RMSE of 963.466, and R² of −0.273. Its negative validation R² indicates that the model does not outperform a validation-mean predictor under the usual R² interpretation.



Residual diagnostics and error-slice analyses help identify potential limitations, including residual dependence and heteroscedasticity. These diagnostics should be interpreted cautiously. The results describe predictive associations rather than causal effects. In addition, same-day weather features may not be available for forecasts made before the day begins.


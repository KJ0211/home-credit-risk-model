# Home Credit Payment Difficulty Modelling

A Jupyter notebook project predicting payment difficulties using
Home Credit application, bureau and repayment records.

## Methods

The notebook creates applicant history features, trains logistic
regression and LightGBM, and evaluates discrimination, calibration,
bootstrap uncertainty and subgroup performance.

It also demonstrates score PSI and feature CSI monitoring.

## Test results

| Model | AUC | Gini | KS | Brier |
| :--- | ---: | ---: | ---: | ---: |
| Logistic regression | 0.7589 | 0.5178 | 0.3890 | 0.0680 |
| LightGBM | 0.7686 | 0.5373 | 0.4026 | 0.0672 |

The paired bootstrap 95% confidence interval for the Gini difference
was 0.0128 to 0.0264 in favour of LightGBM.

## Running the project

Download the Home Credit Default Risk dataset from Kaggle.
Place the extracted CSV files in this project folder.

Install the dependencies listed in requirements.txt.
Start Jupyter from this folder and open 01_home_credit_model.ipynb.
Run the notebook cells in order.

Raw data and generated outputs are excluded from this repository.

## Limitations

Evaluation uses a random stratified holdout rather than a
chronological test. Monitoring compares random samples and does
not establish stability over time.

The target represents the dataset's payment difficulty definition.
This is a portfolio project, not a production lending system.


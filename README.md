# Network Intrusion Detection & Traffic Analysis

Python notebooks exploring network-traffic modeling and intrusion classification through academic experiments.

**Author:** Yassine Razoki · Cybersecurity & Network Infrastructure · EMSI Rabat

## What this project covers

- **Traffic modeling:** simple and multiple linear regression, prediction errors, and residual analysis.
- **Intrusion classification:** logistic regression for binary and multiclass prediction.
- **Data preparation:** categorical encoding, feature scaling, train/test splits, and scikit-learn pipelines.
- **Evaluation:** MAE, MSE, RMSE, R², accuracy, classification reports, and confusion matrices.

These notebooks are learning experiments on tabular datasets. Their results describe the selected data and experimental setup; they do not establish performance on live network traffic.

## Notebook guide

| Notebook | Focus |
| :--- | :--- |
| [Network_Intrusion_Detection.ipynb](Network_Intrusion_Detection.ipynb) | Linear regression on network-traffic features, train/test evaluation, and visualization. |
| [TP1_Regression_Trafic_Reseau.ipynb](TP1_Regression_Trafic_Reseau.ipynb) | Introductory network-traffic regression experiment. |
| [TP_Intrusion.ipynb](TP_Intrusion.ipynb) | Comparison of simple and multiple linear regression, including feature scaling and error metrics. |
| [tp2-2.ipynb](tp2-2.ipynb) | Binary logistic regression using failed logins, connection duration, and transferred data. |
| [tp2-instrusion2.ipynb](tp2-instrusion2.ipynb) | Binary intrusion classification with categorical encoding and a stratified train/test split. |
| [NSL-KDD.ipynb](NSL-KDD.ipynb) | Multiclass logistic regression with a preprocessing pipeline, one-hot encoding, and standardization. |

## Technology stack

Python · pandas · NumPy · scikit-learn · Matplotlib · Seaborn · Jupyter · Google Colab

## Running the notebooks

### Google Colab

Open a notebook on GitHub and use its **Open in Colab** badge. Supply the dataset files expected by that notebook, then execute cells in order.

### Local Jupyter environment

Create a Python environment and install the libraries imported by the notebooks:

```bash
python -m venv .venv
```

Activate it using the command for your operating system:

```powershell
# Windows PowerShell
.\.venv\Scripts\Activate.ps1
```

```bash
# Linux / macOS
source .venv/bin/activate
```

Then install dependencies and launch Jupyter:

```bash
python -m pip install jupyter pandas numpy scikit-learn matplotlib seaborn
jupyter notebook
```

### Dataset requirements

Dataset files are **not included** in this repository.

- Several notebooks load `Test_data.csv` or `Train_data.csv`.
- The NSL-KDD notebook expects `KDDTrain+.txt` and optionally `KDDTest+.txt` or `KDDTest-21.txt`. If a test file is absent, its code creates a train/test split.
- Some paths use Colab's `/content/` directory; adjust them when running locally.
- Match the dataset schema to the notebook's expected columns. The CSV files and the raw NSL-KDD text files are not interchangeable.

## Reading the results

Regression notebooks predict numeric traffic features; classification notebooks predict intrusion labels. Assess them with the metrics appropriate to each task.

For classification, inspect per-class precision, recall, F1-score, and the confusion matrix alongside accuracy. For regression, examine error magnitudes and residual plots alongside R². Dataset age, class imbalance, preprocessing choices, and train/test construction affect how broadly results can be interpreted.

## Related work

[Defense-in-Depth Enterprise Lab](https://github.com/razokiyassine/defense-in-depth-lab) — segmented infrastructure, Suricata IDS, ModSecurity WAF, Active Directory hardening, and MFA.

[GitHub profile](https://github.com/razokiyassine) · [LinkedIn](https://www.linkedin.com/in/yassine-razoki)

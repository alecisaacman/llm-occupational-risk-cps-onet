# LLM-Based Occupational Risk Measurement (CPS + O*NET)

This project develops large language model (LLM)–based measures of occupational risk using textual task descriptions from O*NET and merges those measures into U.S. labor microdata from the Current Population Survey (CPS).

The goal is to demonstrate how LLMs can be used as **measurement tools** in applied economics, rather than as black-box prediction models.

## Motivation
Occupational risk—such as physical danger, income volatility, and exposure to economic downturns—is difficult to measure using standard survey variables. Much of this information is embedded in unstructured occupational descriptions rather than numeric fields.

This project uses LLMs to convert occupational text into structured, interpretable risk indicators that can be used in downstream economic analysis.

## Data Sources
- **O*NET occupational task descriptions** (textual data)
- **U.S. Current Population Survey (CPS)** microdata
- Official **OCC → SOC crosswalks** to merge occupation-level risk measures into worker-level data

Raw microdata are not included due to size and licensing restrictions.

## Methodology
1. Extract textual descriptions of job tasks from O*NET.
2. Prompt LLMs to classify occupations along three risk dimensions:
   - Physical risk
   - Financial liability risk
   - Cyclical job security risk
3. Convert model outputs into Low / Medium / High risk labels.
4. Merge occupation-level risk labels into CPS microdata using occupation crosswalks.
5. Analyze the distribution of occupational risk across workers.

The full pipeline is implemented in a reproducible Jupyter notebook.

## Key Findings
- Approximately one quarter of workers are classified as facing high physical occupational risk.
- Cyclical job security risk is widespread, reflecting exposure to economic downturns rather than on-the-job danger.
- Occupational risk varies substantially across industries and is not well captured by wages alone.

## Files
- `notebooks/occupational_risk_pipeline.ipynb` — full data and LLM pipeline
- `presentation.pdf` — final project presentation summarizing methods and results

## How to Run
1. Open the notebook in Google Colab or Jupyter.
2. Install required Python packages listed in the notebook.
3. Provide local paths to CPS and O*NET data where indicated.
4. Run the notebook top to bottom to reproduce the analysis.

## Notes
This project was completed as part of an advanced applied machine learning course in economics and is intended to demonstrate the use of LLMs for structured measurement in economic research.

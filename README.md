# esg-fin-eda

Reproducible Exploratory Data Analysis on synthetic ESG & Financial Performance data (2000 firms × 9 industries × 2015–2025).

Demonstrates end-to-end analytical workflow: **data generation → cleaning → visualization → insight extraction**.

## Quick Start
bash
git clone https://github.com/sight-link/esg-fin-eda.git
cd esg-fin-eda
pip install -r requirements.txt
python data/gen_sample.py          # generates 2000-row synthetic CSV
jupyter notebook notebooks/eda.py  # or eda.ipynb

## Project Structure
esg-fin-eda/  
├── data/  
│   └── gen_sample.py              # synthetic data generator  
├── notebooks/  
│   └── eda.py                    # main analysis (10 cells)  
├── figs/                          # output visualizations  
│   ├── industry_esg.png  
│   ├── esg_profit.png  
│   ├── region_carbon.png  
│   ├── corr.png  
│   └── resource_esg.png  
├── outputs/  
│   └── summary.csv               # key metrics table  
├── requirements.txt  
└── README.md  

## Key Findings
1、Industry divergence: Finance tops all three ESG pillars; Transport/Energy posts the lowest Environmental scores (synthetic sample, n=1,000, 9 industries)  
2、ESG-profit link: Weak positive correlation (r≈{:.2f}, p<0.01) with pronounced cross-industry heterogeneity  
3、Disclosure-emission decoupling: High-disclosure regions do not map to low emissions — consistent with independent variable generation in synthetic data  
4、Correlation architecture: E/S/G pillars tightly coupled (r>0.7); carbon metrics near-orthogonal to financial indicators  

## Outputs Preview
| Figure | Insight |
|--------|---------|
| ![](figs/industry_esg.png) | Finance dominates ESG; sector gaps visible |
| ![](figs/esg_profit.png) | Scatter + regression by industry |
| ![](figs/region_carbon.png) | Heatmap: Region × Industry carbon intensity |
| ![](figs/corr.png) | Full correlation matrix |

## Tech Stack
`Python 3.10+` · `pandas` · `seaborn` · `matplotlib` · `scipy` · `Jupyter`

## Data Disclaimer
The company_esg_financial_dataset.csv is a synthetic dataset​ published on Kaggle (Shriyash Jagtap, CC BY 4.0). It simulates 1,000 firms × 9 industries × 2015–2025. All findings are illustrative of the analytical pipeline, not empirical ESG facts.

## Author
**sight-link** — Financial Data Analytics | FinTech × ESG Research

*Part of a dual-repo portfolio: [`esg-fintext-demo`](https://github.com/sight-link/esg-fintext-demo) (NLP text classification) + `esg-fin-eda` (tabular EDA)*

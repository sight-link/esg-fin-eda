# esg-fin-eda 📊
Reproducible Exploratory Data Analysis on **synthetic** ESG & Financial Performance data  
(**1,000 firms × 9 industries × 2015–2025**)

Demonstrates end-to-end analytical workflow: **data generation → cleaning → visualization → insight extraction**.

## 📁 Structure
esg-fin-eda/  
├── data/  
│   └── company_esg_financial_dataset.csv 
├── notebooks/  
│   └── esg-fin-eda.ipynb          # main analysis  
├── figs/                          # output visualizations  
│   ├── industry_esg.png  
│   ├── esg_profit.png  
│   ├── region_carbon.png  
│   ├── corr.png  
│   └── resource_esg.png  
└── README.md  

## 📊 Visualizations (synthetic sample, n=1,000)
| Chart | Preview |
|-------|---------|
| Industry ESG scores | ![Industry ESG](figs/industry_esg.png) |
| ESG–Profit relation | ![ESG-Profit](figs/esg_profit.png) |
| Disclosure vs Emission | ![Region Carbon](figs/region_carbon.png) |
| Correlation matrix | ![Corr](figs/corr.png) |
| Resource–ESG | ![Resource](figs/resource_esg.png) |

## 🔑 Key Findings
1. **Industry divergence**: Finance tops all three ESG pillars; Transport/Energy posts the lowest Environmental scores *(synthetic sample, n=1,000, 9 industries)*
2. **ESG–profit link**: Weak positive correlation (**r≈0.18**, p<0.01) with pronounced cross-industry heterogeneity
3. **Disclosure–emission decoupling**: High-disclosure regions do not map to low emissions — consistent with independent variable generation in synthetic data
4. **Correlation architecture**: E/S/G pillars tightly coupled (r>0.7); carbon metrics near-orthogonal to financial indicators

> ⚠️ **Data disclaimer**: `company_esg_financial_dataset.csv` is a **synthetic** dataset (Shriyash Jagtap, Kaggle, CC BY 4.0). All findings illustrate the *analytical pipeline*, not empirical ESG facts.

## 🧰 Stack
Python 3.10+ · pandas · seaborn · matplotlib · scipy · Jupyter

## 🔗 Dual-repo portfolio
- [`esg-fintext-demo`](https://github.com/sight-link/esg-fintext-demo): FinBERT-ESG sentence-level E/S/G classification
- [`esg-fin-eda`](https://github.com/sight-link/esg-fin-eda): tabular EDA + visualization (this repo)

---
sight-link · Financial Data Analytics | FinTech × ESG Research · MIT License

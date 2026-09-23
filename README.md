# ITAI_2277_Group5
Final Project
.
📌 Overview
This project builds an end‑to‑end data engineering, machine learning, and full‑stack application 
that predicts non‑mortgage monthly living costs for residential properties across three major Texas 
counties:
Harris County (48201)

Fort Bend County (48157)

Galveston County (48167)

The system integrates electricity, water/sewer, natural gas, insurance, property taxes, and grocery
cost indices into a unified Master Feature Store and a multi‑output regression model.

The final product is a Streamlit web dashboard that provides cost breakdowns, risk alerts, 
and annual/monthly toggles for homeowners, renters, and analysts.

Project Architecture:
living-cost-model/
│
├── src/
│   ├── clean_data.py          # Data engineering pipeline
│   ├── DataPipeline.py        # Modular transformation pipeline
│   ├── DatabaseManager.py     # ZIP → county lookup + baseline stats
│   ├── model_training.py      # Multi-output ML training
│   ├── inference.py           # predict_monthly_expenses()
│   └── utils/                 # helpers, validators, visualizers
│
├── data/
│   ├── raw/                   # HUD, PUC, TCEQ, RRC, USDA, BLS, TDI
│   └── processed/             # parquet + merged feature tables
│
├── notebooks/                 # EDA, modeling, SHAP, residuals
├── frontend/                  # Streamlit UI
├── docs/                      # Data dictionary, architecture, report
└── README.md

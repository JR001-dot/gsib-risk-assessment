# G-SIB Risk Assessment System

An end-to-end NLP pipeline that analyses quarterly financial reports and earnings call transcripts from Global Systemically Important Banks, extracting regulatory-style risk insights that would take human analysts weeks to compile manually.

**Cambridge Data Science Career Accelerator - Capstone Project (2025)**

---

## Key Results

- **81 quarterly reports** analysed across 3 G-SIBs (UBS, Morgan Stanley, Barclays), 2023-2025
- **5 NLP models** integrated into a single pipeline
- Automated extraction of financial metrics, sentiment trajectories, and emerging risk themes
- Interactive dashboard for regulatory-style exploration of findings

## The Problem

Financial regulators face a growing structural challenge: the volume of unstructured data published by systemically important banks far exceeds what human analysts can process consistently. Key risk indicators are buried in dense financial language, and cross-bank comparisons require synthesising hundreds of pages per quarter.

## Approach

1. **Data Collection** - 81 publicly available quarterly reports and earnings transcripts from three G-SIBs
2. **Multi-Model NLP Pipeline** - FinBERT (domain-specific sentiment), VADER (lexicon-based sentiment), BERTopic (dynamic topic modelling), GPT-2 (contextual summarisation)
3. **Financial Metrics Extraction** - Structured extraction of capital ratios, loss provisions, and liquidity indicators from unstructured text
4. **ARIMA Forecasting** - Time-series projections of key risk indicators
5. **Interactive Dashboard** - Regulatory-style visualisation of sentiment trends, topic evolution, and forecast trajectories

## Technology Stack

| Category | Tools |
|---|---|
| NLP Models | FinBERT, VADER, BERTopic, GPT-2, BART |
| Embeddings | Sentence Transformers |
| Clustering | HDBSCAN |
| Forecasting | ARIMA |
| Data | Pandas, NumPy |
| Visualisation | Plotly, Matplotlib |

## Repository Structure

```
gsib-risk-assessment/
├── README.md
├── requirements.txt
├── notebooks/
│   ├── 01_data_collection.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_sentiment_analysis.ipynb
│   ├── 04_topic_modelling.ipynb
│   ├── 05_metrics_extraction.ipynb
│   └── 06_forecasting_dashboard.ipynb
├── src/
│   └── (utility modules if applicable)
├── data/
│   └── README.md  # data sources and access instructions
└── images/
    └── (key visualisations)
```

## Important Note

This is a prototype built using only publicly available financial data. It demonstrates the methodology and capability, not a production deployment.

## Case Study

Full write-up with methodology and results: [rjdatavoyage.co.uk/projects/gsib-risk-assessment](https://rjdatavoyage.co.uk/projects/gsib-risk-assessment/)

## Author

**Raquel J.** - [RJ Data Voyage](https://rjdatavoyage.co.uk) | [LinkedIn](https://www.linkedin.com/in/raquel-j-664113153/)

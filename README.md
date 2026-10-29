# G-SIB Disclosure Analysis Prototype (team project)

NLP prototype that turns public bank disclosures into comparable sentiment and risk signals across banks and quarters.

**Origin:** University of Cambridge Data Science Career Accelerator employer project (2025), team project. **My role:** I designed and built the core pipeline in this notebook. The LLM summarisation module (Section 3) was built by a teammate; the wider team contributed brainstorming and validation. **Data:** public documents; bank names and files withheld. Notebook outputs cleared; figures below come from the original run.

## What was done
- 81 public documents (earnings reports and earnings-call / Q&A transcripts) for three Global Systemically Important Banks (Bank A, Bank B, Bank C), Q1 2023 to Q1 2025 - 27 per bank.
- Text extraction and chunking; FinBERT and VADER sentiment on every chunk.
- Regex extraction of financial metrics (capital ratios, net interest margin, returns).
- Keyword-based risk taxonomy (credit, market, liquidity, operational, legal and others).
- GPT-2 document insights and BART-based summary aggregation; HTML reports and a dashboard image.

## Results
- 17,292 text chunks scored: 65.2% neutral, 19.1% positive, 15.8% negative (FinBERT).
- Share of negative chunks by bank: Bank A 20.0%, Bank C 11.2%, Bank B 9.2%; stable across quarters (14.1% to 16.9%).
- Leading themes in negative chunks: credit risk (10.0%), treasury / balance sheet (7.1%), cost inflation (4.6%), market volatility (4.1%), legal risk (3.5%); 36.7% unclassified.
- 358 financial metric mentions, 381 risk assessments and 345 transcript segments extracted.

## Limitations
- Prototype: extracted metrics were not validated against the filings, so they are not used for capital-ratio comparisons.
- BERTopic was attempted but returned a single topic on this corpus; the themes above come from the keyword taxonomy.
- An ARIMA projection module is included in the code but was not run in this version, and nine quarterly points per bank would be too few for it.
- An exploratory section that used illustrative (non-real) inputs has been removed.

## Tech stack
Python, Hugging Face Transformers (FinBERT, GPT-2, BART), VADER, sentence-transformers, BERTopic (attempted), pandas, Plotly, Matplotlib

## Repository
- `gsib_risk_assessment.ipynb`
- `requirements.txt`

---

**Author:** Raquel J. | [rjdatavoyage.co.uk](https://rjdatavoyage.co.uk)

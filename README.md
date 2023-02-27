# GAAP Implementation Tracker

Track how U.S. public companies implement complex accounting standards, using SEC EDGAR public data.

## The problem

FASB issues accounting standards. Those standards work for routine transactions. But when a deal combines derivatives with leases, or when a consolidation question involves shared control, the standard does not give a clear answer. Every practitioner develops their own interpretation. The result: companies with identical economics end up with different financial statements.

This dashboard tracks those differences.

## What it tracks

**Topic 832 (Government Grants)** — A new standard affecting every company receiving CHIPS Act, IRA, or infrastructure funding. Tracks adoption patterns, recognition method elections, and disclosure approaches as companies begin implementation.

**ASC 815 (Derivatives & Hedging)** — One of the most complex areas of U.S. GAAP. Analyzes disclosure patterns and derivative positions across SEC filers using XBRL data.

**Restatement Patterns** — Which accounting standard areas produce the most financial reporting errors, tracked through amended SEC filings.

## Live dashboard

[View the dashboard](https://gaap-tracker.streamlit.app) (Streamlit Cloud)

## Run locally

```bash
git clone https://github.com/placeholder/gaap-tracker.git
cd gaap-tracker
pip install -r requirements.txt
streamlit run app.py
```

## Data sources

All data comes from free SEC EDGAR public APIs. No paid data sources. No API key required.

- **EFTS** — Full-text search across all SEC filings
- **XBRL Frames** — Structured financial data across all filers
- **Company Facts** — Detailed XBRL data for individual companies

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT

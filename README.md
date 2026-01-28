# GAAP Implementation Tracker

Track how U.S. public companies implement complex accounting standards, using SEC EDGAR public data.

**[Live dashboard →](https://gaap-tracker.vercel.app)**

## The problem

FASB issues accounting standards. Those standards work for routine transactions. But when a deal combines derivatives with leases, or when a consolidation question involves shared control, the standard does not give a clear answer. Every practitioner develops their own interpretation. The result: companies with identical economics end up with different financial statements.

This dashboard tracks those differences.

## What it tracks

11 areas of U.S. GAAP, plus enforcement actions and federal grants:

| Area | Description |
|------|-------------|
| **Topic 832** | Government grant accounting under the CHIPS Act, IRA, and infrastructure programs |
| **ASC 815** | Derivatives classification, hedge accounting, and effectiveness testing |
| **ASC 820** | Fair value hierarchy (Level 1/2/3) and unobservable input disclosures |
| **ASC 810** | Variable interest entity analysis and consolidation decisions |
| **ASC 842** | Operating vs. finance lease classification and right-of-use assets |
| **ASC 606** | Five-step revenue model, performance obligations, and contract modifications |
| **ASC 326** | CECL methodology and lifetime credit loss estimation |
| **ASC 718** | Stock option valuation, RSU accounting, and compensation expense |
| **ASC 740** | Deferred tax positions, valuation allowances, and uncertain tax positions |
| **ASC 350** | Goodwill impairment testing and reporting unit determination |
| **Restatements** | Amended filings disclosing corrections to previously issued financials |

Plus: **SEC enforcement actions** and **federal grants** (CHIPS Act, IRA, IIJA) tracked via USAspending.gov.

## How it works

1. **Search SEC filings** — EDGAR Full-Text Search API finds 10-K and 10-Q filings referencing specific standards
2. **Extract patterns** — Footnote disclosures are classified by recognition method, measurement technique, and presentation format
3. **Track differences** — Cross-company and cross-industry comparisons surface where identical economic transactions produce different accounting treatments

## Tech stack

- **Frontend**: Next.js 14, React 18, TypeScript
- **Styling**: Tailwind CSS, Tremor UI
- **Charts**: Recharts, react-simple-maps (US map)
- **Data**: SEC EDGAR EFTS, XBRL Frames, USAspending.gov
- **Deployment**: Vercel

## Run locally

```bash
git clone https://github.com/zgu-usgaap-fr/GAAP-Implementation-Toolkit.git
cd GAAP-Implementation-Toolkit
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Legacy Streamlit app

The original prototype is still available:

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Data sources

All data comes from free public APIs. No paid data sources. No API key required.

- **EFTS** — SEC EDGAR Full-Text Search across all filings
- **XBRL Frames** — Structured financial data across all filers
- **Company Facts** — Detailed XBRL data for individual companies
- **USAspending.gov** — Federal grant and award data

Data refreshes every 6 hours.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

MIT

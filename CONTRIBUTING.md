# Contributing

Contributions welcome. This project tracks how U.S. public companies implement complex accounting standards using SEC EDGAR public data.

## Setup

```bash
npm install
npm run dev
```

## How to contribute

1. Fork the repo
2. Create a branch (`git checkout -b feature/your-feature`)
3. Make your changes
4. Run the build (`npm run build`) and lint (`npm run lint`)
5. Submit a pull request

## What we need

- **New ASC topic analyses** — add an area page for an accounting standard not yet covered
- **Disclosure classification improvements** — better parsing of footnote text to identify accounting method choices
- **Data quality fixes** — corrections to how filings are categorized or classified
- **Chart and visualization improvements** — better ways to surface implementation patterns
- **Documentation** — clearer methodology descriptions

## Project structure

```
src/
  app/                  # Next.js pages (App Router)
    areas/[slug]/       # Dynamic area detail pages
    enforcement/        # SEC enforcement actions
    federal-grants/     # Federal grants tracking
    overview/           # Overview dashboard
    about/
  components/
    charts/             # Recharts visualizations
  lib/
    areas/              # Area registry, types, data loading
    edgar/              # EDGAR API clients (EFTS, XBRL)
public/data/            # Pre-fetched JSON datasets
data/                   # Python data pipeline (legacy)
pages/                  # Streamlit pages (legacy)
scripts/                # Data refresh scripts
```

## Data sources

All data comes from SEC EDGAR public APIs and USAspending.gov. No paid data sources. No proprietary content.

- EFTS (full-text search): `https://efts.sec.gov/LATEST/search-index`
- XBRL Frames: `https://data.sec.gov/api/xbrl/frames/`
- Company Facts: `https://data.sec.gov/api/xbrl/companyfacts/`
- Federal grants: `https://api.usaspending.gov/`

## Code style

- TypeScript strict mode
- Functional components, server components by default
- Tailwind utility classes, Tremor UI components
- No unnecessary abstractions

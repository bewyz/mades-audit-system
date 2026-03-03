# MADES — Internal Audit Analysis System

A browser-based analytics dashboard for processing and analyzing internal hygiene audit reports. Built as a single HTML file — no installation, no backend, no dependencies except a modern browser.

**[→ Live Demo](https://bewyz.github.io/mades-audit-system)**



![Dashboard Preview](preview.png)

---

## What It Does

Audit teams generate PDF reports for each store inspection. This system automates the analysis:

1. **Upload PDFs** → automatic parsing (store name, inspector, date, findings)
2. **View Dashboard** → KPIs, coverage rate, ranking, risk distribution
3. **Trend Analysis** → month-over-month improvement/deterioration per store
4. **Heatmap** → Store × Category matrix, color = issue density
5. **Chronic Issues** → findings that repeat across multiple periods or stores
6. **Regional Comparison** → BSY → BY → Store drill-down hierarchy
7. **Action Tracking** → auto-generated or manual actions with deadlines
8. **Excel Export** → period summary, chronic issues, action list, full detail

---

## Key Features

| Feature | Details |
|---------|---------|
| PDF Parsing | Automatic extraction via PDF.js — store, inspector, date, findings |
| Hierarchy | 4 regional managers → 28 area managers → 273 stores |
| Coverage KPI | How many stores inspected this period, which areas are missing |
| Multi-period | Load January, February, March separately — trend auto-calculates |
| Chronic Detection | Same finding in 2+ periods or 3+ stores flagged automatically |
| Auto Actions | System generates action items from critical findings |
| Backup/Restore | JSON export/import — no data loss on browser clear |
| Management | Add/edit/delete stores, area managers, regional managers |

---

## Tech Stack

- **Vanilla JavaScript** — no frameworks
- **PDF.js** (CDN) — client-side PDF parsing
- **localStorage** — persistent data storage
- **Single HTML file** — zero build process, works offline

---

## Running Locally

```bash
# Clone
git clone https://github.com/your-username/mades-audit-system.git

# Open directly in browser — no server needed
open index.html
```

Or deploy to **GitHub Pages**:
- Repo Settings → Pages → Source: `main` branch → `/root`
- Live at: `https://your-username.github.io/mades-audit-system`

---

## Usage

### Loading Reports
1. Go to **Rapor Yükle** (Upload)
2. Enter period: `03.2026`
3. Drag & drop PDF files
4. Click **İşle ve Kaydet** (Process & Save)

### Data Privacy
The demo version contains anonymized data (MAGAZA_001, Bölge Yöneticisi 01, etc.).  
For production use, replace with your actual store hierarchy via the **Yönetim** (Management) page.

---

## Project Background

Built to solve a real operational problem: audit teams were generating PDF reports that sat unread because analysis was too time-consuming. This dashboard reduces time-to-insight from hours to seconds.

**Scope:** 273 stores across Istanbul and Ankara, monthly inspection cycles, 4-tier management hierarchy.

---

## Screenshots

| Dashboard | Heatmap | Trend |
|-----------|---------|-------|
| Coverage KPI, ranking | Store × Category matrix | Month-over-month change |

---

## License

MIT — free to use and adapt.

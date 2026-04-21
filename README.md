# Construction Operations Analytics Dashboard

A multi-page Power BI dashboard built as a proof of concept for K&R Ops & Analytics (KROA), targeting construction and field service businesses. Tracks job profitability, schedule performance, and phase-level bottlenecks across 50+ projects and 250 phase events.

## Tech Stack
- Power BI (DAX, Power Query)
- Python (Pandas, NumPy) for synthetic data generation
- Star schema data model

## Dashboard Pages
- **Cover Page** — Project overview and navigation
- **Executive Summary** — High level KPIs across all projects
- **Project Deep Dive** — Individual job exploration with drill-downs
- **Financial Analysis** — Profitability, budget variance, and cost breakdown

## Data Model
Star schema with 6 tables:
- **FactJobs** — Core job financials and schedule data
- **FactPhases** — Phase level progression and delay tracking
- **DimClient** — Client segments and details
- **DimPM** — Project manager information
- **DimRegion** — Geographic region data
- **DimDate** — Date table for time intelligence

## Key DAX Measures
- `Profit Margin %` — Profit as a percentage of contract value using DIVIDE
- `Budget Variance` — Actual cost vs estimated cost
- `On-Time Completion Rate` — Percentage of jobs completed on schedule
- `Phase Delay Tracking` — Average days delayed per phase
- `Total Contract Value` — SUM of all job contract values
- `Average Days Delayed` — AVERAGEX across delayed jobs

## Data Generation
Synthetic dataset generated using Python. Run the Jupyter notebook to recreate all CSVs:

```
jupyter notebook generate_data.ipynb
```

## Purpose
Built to demonstrate end to end analytics capability for KROA client demos and as a portfolio piece targeting data analyst roles in Edmonton.
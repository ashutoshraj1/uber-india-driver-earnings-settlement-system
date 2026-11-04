# Uber India Driver Earnings & Trip Settlement System

A SQL Developer portfolio project focused on driver earnings, weekly payout settlement, cash collection offsets, commissions, incentives, and reconciliation controls.

> **Project context:** This repository implements a simulated product scenario using a deterministic July 2026 dataset, a temporary local API simulator, and SQLite. It is an independent portfolio exercise. It is **not** an Uber production system, does not use confidential Uber data, and does not represent employment, endorsement, or an official engagement with Uber.

## Repository structure

```text
uber-india-driver-earnings-settlement-system/
├── README.md
├── .gitignore
├── Developer/
│   └── SQL_Developer_Uber_India_Driver_Earnings_and_Trip_Settlement_System.ipynb
├── Instructor/
│   └── Instructor_Solution_Uber_India_Driver_Earnings_and_Trip_Settlement_System.ipynb
└── Product_Document/
    ├── PRD_Uber_India_Driver_Earnings_and_Trip_Settlement_System.docx
    └── Meeting_Transcript_Uber_India_Driver_Earnings_and_Trip_Settlement_System.docx
```

## Business problem

The scenario models a payout-control workflow in which trip earnings, vehicle-based commission, cash already collected by drivers, approved incentives, payout batches, and bank-transfer events must be reconciled. The SQL layer identifies missing or incorrect transfers and other settlement exceptions in a repeatable way.

## Scope and implementation

- **Role:** SQL Developer
- **Runtime:** Google Colab
- **Database:** SQLite
- **Dataset:** Deterministic, locally generated July 2026 activity
- **API:** Temporary local simulator; no live or public Uber API
- **Seven core tables:** `drivers`, `commission_rules`, `trips`, `incentives`, `payout_batches`, `payout_items`, `payout_transfers`
- **Three system-managed tables:** `driver_ledger`, `settlement_exceptions`, `api_ingestion_runs`

### Work demonstrated

1. Relational database design, primary/foreign keys, constraints, indexes, and ER diagram.
2. API consumption and validation using GET, POST, PUT, PATCH, and GET → DELETE → GET.
3. Thirteen SQL analyses covering joins, aggregation, HAVING, anti-joins, set operations, CTEs, subqueries, window functions, ranking, running totals, moving averages, and LAG.
4. Transaction integrity using one committed adjustment and one rolled-back adjustment.
5. Weekly payout reconciliation and exception reporting.
6. Seven-step workflow automation design and cron-expression validation.
7. Git collaboration and safe database-change workflow diagrams.

## How to use

### Developer notebook

Open the notebook in Google Colab and run the setup cells. Complete the cells marked `SQL DEVELOPER WORKSPACE` and `TODO`. Expected outputs and validation helpers are included.

### Instructor solution

Use the Instructor notebook as the completed reference implementation. It contains the filled solutions and recorded execution outputs.

The two notebooks preserve the same **111-cell structure and order**. All **72 Markdown cells match exactly**; the solution fills the Developer workspaces in the corresponding code cells.

## Validation snapshot

The included Instructor notebook's saved execution outputs show:

- `SETUP COMPLETE`
- All **26 activity IDs** marked **Passed**
- Completion summary: **26 Passed**
- No saved Python exception outputs

The 26 activities cover ER-1, API-Q1 to API-Q5, Q1 to Q13, T1/T2, AUTO-FLOW/AUTO-REPORT/AUTO-CRON, and ENG-GIT/ENG-CHANGE.

## Product documents and dates

The July 2026 dataset is treated as a retrospective review dataset. The operational review and product/engineering handover are dated **3 November 2026**; the PRD is finalized on **4 November 2026**, the same date this portfolio package is prepared for upload. This keeps the review, handover, documentation, and upload chronology consistent.

The stakeholder names and handover conversation are part of the supplied scenario documents. They are not evidence of a real Uber meeting or actual company stakeholders.

## Technology

`SQL` · `SQLite` · `Python` · `Requests` · `Google Colab` · `REST API concepts`

## Limitations

- No live Uber API or production credentials are used.
- No confidential or proprietary Uber dataset is included.
- The API is a temporary local simulator created for the notebook runtime.
- Cron expressions are validated as scheduling definitions; a stopped Google Colab runtime cannot host a persistent cron daemon.
- This repository demonstrates SQL and data-control concepts in a reproducible portfolio simulation.

## Notebooks

| Notebook | Description | Link |
|---|---|---|
| Developer Notebook | SQL exercises and implementation workspace | [Open in Google Colab](https://colab.research.google.com/github/ashutoshraj1/uber-india-driver-earnings-settlement-system/blob/main/Developer/SQL_Developer_Uber_India_Driver_Earnings_and_Trip_Settlement_System.ipynb) |
| Instructor Solution | Completed SQL implementation with execution outputs | [Open in Google Colab](https://colab.research.google.com/github/ashutoshraj1/uber-india-driver-earnings-settlement-system/blob/main/Instructor/Instructor_Solution_Uber_India_Driver_Earnings_and_Trip_Settlement_System.ipynb) |

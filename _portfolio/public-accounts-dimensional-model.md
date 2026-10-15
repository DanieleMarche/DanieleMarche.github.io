---
title: "Dimensional models for monitoring public-sector cash transactions"
excerpt: "Designed the fact schemas and analysis models, in the Dimensional Fact Model, for new reports that track public bodies' provisional (not yet regularised) cash movements. Implemented in SAP BusinessObjects. Internship project, described in my Bachelor's thesis."
collection: portfolio
order: 3
kind: thesis
---

**Sopra Steria Italia** · Data analyst intern · Public administration · 2025

*This project is described in full in my Bachelor's thesis at Sapienza, "Conceptual modelling as a governance tool in data warehousing processes".*

### The domain

When an Italian public body receives or pays money without the proper accounting order, the movement is still recorded, under a provisional code. These provisional movements must later be **regularised** with a definitive accounting code.

A major government body wanted to check that public bodies regularise them correctly and on time. That meant two new reports on an existing data warehouse:

- provisional movements **still not regularised** after a given time;
- regularised movements whose transactions **don't match** between the payment records and the body's own accounts.

### My role

In the last month of my internship, together with my company tutor, I did the **conceptual modelling** for the whole change, and we were the reference for the people implementing it.

- With the stakeholders, we analysed the information needs and identified the **facts, measures, dimensions and descriptive attributes**.
- I modelled **three fact schemas** in the **Dimensional Fact Model (DFM)** using Indyco Builder:
  - **Provisional movement:** amount, reversed amount, restored and regularised amounts;
  - **Unregularised provisional movements:** amount and amount still to regularise;
  - **Provisional movements with anomalies:** one row per transaction, at a finer grain.
- The three schemas share the warehouse's common dimension hierarchies (public body, financial year, bank, local-government classification, calendar date). We also introduced **one new hierarchy** needed by the physical implementation.
- I modelled the **analysis features** behind each report: which fact schemas, measures, dimensions and attributes each report uses.
- We validated everything with the functional leads and documented it.

### From model to reports

- The new fact schemas were added to the existing **SAP BusinessObjects universe** on public-sector spending, using the Information Design Tool.
- The reports were built in **SAP Web Intelligence**. We checked that they stayed consistent with the model and proposed changes to how the data was shown.

*The data is sensitive, so the thesis and this page describe the model at a high level only.*

<hr>

### Technologies used

- **Modelling:** Dimensional Fact Model, Indyco Builder
- **BI:** SAP BusinessObjects (Information Design Tool, Web Intelligence)
- **Data:** data warehouse / data mart, ETL

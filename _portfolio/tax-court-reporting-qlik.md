---
title: "Tax-court reporting rebuilt in Qlik Sense"
excerpt: "Restructured the data model and redesigned the Qlik Sense reports on Italy's tax courts: caseloads, case values, judges and average trial length. Internship project, described in my Bachelor's thesis."
collection: portfolio
order: 1
kind: thesis
---

**Sopra Steria Italia** · Data analyst intern · Public administration · 2025

*This project is described in full in my Bachelor's thesis at Sapienza, "Conceptual modelling as a governance tool in data warehousing processes".*

This was my first project at Sopra Steria. The client publishes yearly reports on Italy's **tax courts** (*Corti di Giustizia Tributaria*), the courts that decide disputes between taxpayers and the tax authorities. The reports cover how many cases come in, are closed and are still pending, what they are worth, how many judges each court has, and how long a case takes on average.

The reports ran in Qlik Sense, but the data model behind them had been generated automatically by the tool. The client asked for two things: a business layer they could control, and a full redesign of the dashboards.

### 1. Renaming the semantic layer

In Qlik Sense, the field names in the data model are the names end users see. I analysed every table and field and renamed them after the business concepts they represent (cases received, cases closed, pending cases, outcomes, average duration, judges, value bands, digital filings, territory).

### 2. Rebuilding the data model

- I worked out the **grain** of each table. Five of them (cases received, closed and pending, average duration, judges) shared the same grain: **report year × year × court**.
- I merged those five into a single logical table with **full outer joins**, so no row from any source table was lost.
- The more detailed tables (digital filings by type, pending digital archives by type, cases by value band) stayed separate. I linked them through Qlik's **associative model** on the composite key court + report year + year, which avoids unwanted synthetic keys.
- At the client's request, I added a **province → court** table to the territory dimension, so the reports could show maps.

<img src="/images/thesis/qlik-associations.png" alt="Qlik Sense data model after the restructuring: one central table linked to the territory table and to four more detailed tables" style="width: 100%; height: auto;">
*The data model after the restructuring (Qlik Sense model viewer).*

<img src="/images/thesis/qlik-associations-fields.png" alt="Table view of the Qlik Sense data model showing the fields of each table and the keys that link them" style="width: 100%; height: auto;">
*The same model with field-level detail.*

### 3. Redesigning the reports

- I reorganised all the report scripts around **master items and variables**, so each formula is defined once and reused everywhere. Later changes became much faster and safer.
- I redesigned the layout from scratch, with clearer navigation and new dynamic charts.
- I added **geographic maps**, made possible by the new province table.

We validated the work with the client every one or two weeks.

<hr>

### Technologies used

- **BI:** Qlik Sense (data load scripts, associative model, master items, variables, maps)
- **Modelling:** grain analysis, semantic layer design

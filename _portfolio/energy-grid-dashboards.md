---
title: "Energy grid analytics on a data lake"
excerpt: "Three end-to-end Power BI dashboards for an energy company, built on layers of SQL views in Dremio over tables of tens of millions of rows. Sopra Steria, 2025–2026."
collection: portfolio
order: 1
kind: confidential
---

**Sopra Steria Italia** · Data Analyst · Energy sector · 2025 – 2026

I built and maintained three Power BI dashboards end to end for a client in the energy sector. I worked on the whole chain, from the raw tables in the data lake to the visuals the business users work with.

### What I built

- **Grid reliability** across **6 countries** (Italy, Spain, Argentina, Brazil, Chile, Colombia): outages and faults measured through the standard indicators SAIDI, SAIFI and CAIDI.
- **Logistics**: stock, turnover and consumption, with price, volume and FX effects, and conversion from local currencies to EUR.
- **Installed grid materials**.

### How

- I wrote the transformations as **layers of SQL views in Dremio**, over tables with **tens of millions of rows**. The views feed Power BI datasets of **5M+ rows** each.
- I **validated the data** reaching Dremio, and our own transformations, against the **source SAP tables**.
- I also maintained two more dashboards (contracts and network topology), fixing and extending them based on user feedback.
- I was one of the first in my team to adopt **AI-assisted development with MCP servers**, and the **PBIP format**, which lets us version Power BI reports in Git.

<hr>

### Technologies used

- **Data:** Dremio data lake, SQL, SAP (source systems)
- **BI:** Power BI (DAX), PBIP + Git

*Client data and screenshots are confidential, so this page describes the work without showing it.*

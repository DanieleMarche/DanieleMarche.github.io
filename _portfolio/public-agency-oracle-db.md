---
title: "Database for a government agency's asset-disposal platform"
excerpt: "Designed and implemented in Oracle the database behind a web app a national agency uses to give away its unused IT assets through public calls. From requirements to ER model, relational schema and SQL. Internship project, described in my Bachelor's thesis."
collection: portfolio
order: 2
kind: thesis
---

**Sopra Steria Italia** · Data analyst intern · Public administration · 2025

*This project is described in full in my Bachelor's thesis at Sapienza, "Conceptual modelling as a governance tool in data warehousing processes".*

A national government agency wanted a web application to **dispose of IT assets it no longer uses**, by giving them to public bodies and associations through public calls. Within the project team, under the project manager, **I was responsible for the database**, which was the first step of the project.

### What the application does

- The agency's **central office** creates calls and approves the rankings.
- **Regional offices** pick the assets to give away, group them into **lots**, manage the rankings and track the handover to the winners.
- **External organisations** apply to one or more calls.

Once live, the system is expected to serve up to **tens of thousands of external users** plus the agency's staff.

### Conceptual model

I started from the client's specification document (use cases, activity diagrams, functional and non-functional requirements) and turned it into an **ER diagram** with (min, max) cardinalities, strong and weak entities, grouped into six areas: calls, assets, users, offices, territory and FAQ.

<img src="/images/thesis/asset-db-er-conceptual.png" alt="Conceptual ER diagram of the database, with entities grouped into users, offices, territory, call management, assets and FAQ" style="width: 100%; height: auto;">
*Conceptual ER diagram (client-identifying names removed).*

I then defined the domain constraints and, together with the client, the **allowed states and transitions** of calls, rankings and applications.

<img src="/images/thesis/asset-db-state-flow.png" alt="State flow diagram: a call goes from draft to open to closed, its rankings from to-be-calculated to provisional to published, and applications from draft to submitted to ranked" style="width: 100%; height: auto;">
*How calls, rankings and applications move through their states.*

### Relational schema and design choices

<img src="/images/thesis/asset-db-relational.png" alt="Final relational diagram of the database" style="width: 100%; height: auto;">
*Final relational schema (project-specific table prefix removed).*

Translating the ER model into tables meant a few deliberate choices:

- **Assets denormalised into one table**, loaded by an ETL process the client runs from another database. To avoid interfering with that process, I tracked which asset belongs to which call and lot in a **separate associative table** instead of adding columns to it.
- **1:1 relationships merged** into single tables (lot + ranking, application + its ranking entry).
- **Surrogate keys** with Oracle **sequences** for calls and lots, and key–description lookup tables for every state and type. This keeps the schema open to new grouping rules decided later.
- **Users, offices and territory** reuse tables the client already maintains, instead of duplicating them. A user-permissions table records who can access what.
- **Cross-table integrity rules** are enforced in the back end, as agreed with the team.

### Implementation and documentation

I wrote the **SQL DDL** (tables, keys, sequences), organised by type in the project repository, and the **technical documentation**: every table and field, data types, naming conventions, and the reason behind each design choice. We used it in the validation sessions with the client.

<hr>

### Technologies used

- **Database:** Oracle, SQL, Oracle SQL Developer
- **Modelling:** ER (conceptual) and relational modelling, draw.io

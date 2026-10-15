---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<a href="{{ base_path }}/files/daniele-marchetilli-cv.pdf" class="btn btn--primary"><i class="fas fa-download" aria-hidden="true"></i> Download CV (PDF)</a>

MSc Computer Science student (Computer Systems and Infrastructure track) at the University of Amsterdam & VU Amsterdam, with over a year as a data engineer at Sopra Steria, building SQL pipelines, data models and BI dashboards on datasets of millions of rows. **I'm looking for a software, systems or data engineering internship, full-time from January 2027, for 3–6 months.**

Education
======
* **M.Sc. in Computer Science (joint degree)**, University of Amsterdam & Vrije Universiteit Amsterdam, Sep 2026 – expected Jul 2028
  * Track: Computer Systems and Infrastructure
  * Courses: Programming Large-Scale Parallel Systems (Julia), Performance of Networked Systems; from 2027: Distributed Algorithms, Web Services and Cloud-Based Systems, Accelerator-Centric Computing Ecosystems
* **B.Sc. in Computer Science (Informatica)**, Sapienza University of Rome, Sep 2022 – Oct 2025
  * Final grade: 102/110
  * Thesis: conceptual modelling for data warehousing, based on my internship at Sopra Steria
  * Erasmus+ exchange semester at Universidad Carlos III de Madrid (Sep 2024 – Jan 2025)

Experience
======
**Sopra Steria Italia**, Data Engineer (intern, then apprentice), Rome, Mar 2025 – Aug 2026

*Energy sector (Dremio data lake, SQL, Power BI)*

* Built and maintained 3 Power BI dashboards end to end. I wrote the transformations as layers of **SQL views in Dremio** over tables with **tens of millions of rows**, feeding Power BI datasets of **5M+ rows** each:
  * grid reliability in **6 countries** (IT, ES, AR, BR, CL, CO): outages and faults through SAIDI, SAIFI and CAIDI
  * logistics: stock, turnover and consumption, price/volume/FX effects, local-currency-to-EUR conversion
  * installed grid materials
* Validated the data reaching Dremio, and our transformations, **against the source SAP tables**
* Maintained 2 more dashboards (contracts, network topology), fixing and extending them based on user feedback
* Early adopter in the team of AI-assisted development with MCP servers, and of the PBIP format for Git-versioned Power BI reports

*Public administration*

* **Designed and implemented a new Oracle database** for a national government agency to manage the reuse and transfer of its technology assets. I turned loosely defined functional requirements into the conceptual model, the physical model and the implementation. Once live, it should serve up to **tens of thousands of external users** plus agency staff.
* Maintained the dimensional-model repository of a data warehouse: updated existing star schemas and added new ones
* Wrote **Python scripts** that parse SAP BusinessObjects universe exports and match objects across universes, to find overlaps and universes to merge or optimise. They **replaced hours of manual review**.
* Designed from scratch the **star schemas** behind 2 Qlik Sense dashboards on tax-court data (up to 100K+ rows)
* Built the first module of a Python generator for data-warehouse change-specification documents, saving several hours per document

Projects
======
* **[myTransferApp](/portfolio/my-transfer-app/)** (C, Linux): client/server file transfer over sockets, using multiprocessing and multithreading
* **[MyFinger](/portfolio/my-finger/)** (C, Linux): re-implementation of Unix `finger`, reading user data from Linux system files
* **[MyBank](/portfolio/my-bank-crypto/)** (Python, PostgreSQL): app that protects user data with symmetric/asymmetric encryption and signatures
* **[JBomberman](/portfolio/portfolio-1/)** (Java): Bomberman clone built on OOP and design patterns

Skills
======
* **Programming:** Python, SQL, C, Java, Julia
* **Data & BI:** dimensional modelling, Oracle, PostgreSQL, Dremio, Power BI (DAX), Qlik Sense, SAP BusinessObjects
* **Systems & tools:** Linux, Git, sockets and concurrency in C, parallel programming
* **Languages:** Italian (native), English (C1, IELTS 7.5), Spanish (B1)

Part-time jobs
======
Alongside my studies:

* Orientation desk at Sapienza University of Rome, Feb – Aug 2024
* Infopoint employee, PTA Group, May – Aug 2024
* Waiter, La Masseria, Rome, Jun 2021 – Apr 2024

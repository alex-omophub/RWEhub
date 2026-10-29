# 02 · Curated Repository Catalog

Full annotations for the 15 repositories under GitHub's
[`rwe` topic](https://github.com/topics/rwe), grouped by learning track.
Star counts are a snapshot from mid-2026 and will drift — treat them as a rough
signal, not a ranking.

Legend: ⭐ = recommended starting point for the track.

---

## Track 1 — Data & OMOP CDM

### ⭐ databricks-industry-solutions/omop-cdm · Python · ~29★
Unlocking the power of health data with a modern data lakehouse. The most
mature repo in the topic and the best entry point for the OMOP CDM. Shows how to
land and standardize health data at scale on Databricks.
<https://github.com/databricks-industry-solutions/omop-cdm>

### eyedress02/modern-lakehouse · Shell
Build a modern data lakehouse with MinIO, MariaDB, and Dremio. Useful if you
want an open-source, self-hostable alternative to the Databricks stack for
storing RWD.
<https://github.com/eyedress02/modern-lakehouse>

### ericg1212/healthcare-claims-pipeline · Python
Pipeline that processes HL7 **FHIR** data through the **OMOP CDM**, with claims
classification and RWE cohort analysis. Great for seeing the ingestion path from
interoperability standards to analyzable cohorts.
<https://github.com/ericg1212/healthcare-claims-pipeline>

### aminyakubu/explorys · R
R package to quickly pull demographic and clinical characteristics from the IBM
Explorys database. A concrete example of a source-specific data-access layer.
<https://github.com/aminyakubu/explorys>

### OMOPHub/omophub-python · Python
Python SDK for the OMOPHub API, which serves the OHDSI standardized vocabularies
(SNOMED CT, ICD-10, LOINC, RxNorm and 120+ more). Shows how source codes are
looked up and mapped to OMOP standard concepts during ETL, without downloading
and loading Athena locally.
<https://github.com/OMOPHub/omophub-python>

---

## Track 2 — Reproducibility & Study Lifecycle

### ⭐ janickweberpals/icpe-git-2024 · HTML · ~4★
Course materials for *"Let's git it started: transparency and reproducibility
across the RWE study lifecycle"* (ICPE 2024). The best on-ramp for the
version-control and transparency practices RWE demands.
<https://github.com/janickweberpals/icpe-git-2024>

### repro-stats/reproducr-rwe · R
End-to-end **reproducr** pipeline for a simulated RWE study: PS matching, IPTW,
Cox PH, Kaplan–Meier, `renv` locking, and an academic audit report. This is the
reference implementation that ties Tracks 2 and 3 together — run it in Week 3.
<https://github.com/repro-stats/reproducr-rwe>

### janickweberpals/agentic-code-review-ispe-2026 · R
Presentation on **agentic code review** for analytics (ISPE 2026). Forward-looking
look at using AI agents to QC analysis code — relevant to how CABS works.
<https://github.com/janickweberpals/agentic-code-review-ispe-2026>

---

## Track 3 — Methods & Causal Inference

### ⭐ al8xi8/EPID708_UMich2025 · R
Coursework covering **machine learning for epidemiologic analysis** with a
causal-inference focus (University of Michigan, 2025). Solid, structured
grounding in the methods that make RWE credible.
<https://github.com/al8xi8/EPID708_UMich2025>

### htlin222/roche-vabysmo-rwe-workshop · R
Interactive textbook teaching clinical RWE analysis methods using R and AI, built
around a Roche/Vabysmo workshop. Bridges methods and a real therapeutic context.
<https://github.com/htlin222/roche-vabysmo-rwe-workshop>

---

## Track 4 — Applied Case Studies & Portfolios

### Krashnika-Deivakumar/aml-flt3-market-sizing · R · ~1★
Real-world data simulation for **AML** (acute myeloid leukemia, FLT3) market
sizing and survival analysis. A commercial/HEOR-flavored application of RWE.
<https://github.com/Krashnika-Deivakumar/aml-flt3-market-sizing>

### natsousa/rwbiomarker · R
RWE **biomarker** analysis focused on **colon cancer**. Compact domain example.
<https://github.com/natsousa/rwbiomarker>

### kousha1234/Research-portfolio · R
Evidence and R Markdown research portfolio built on synthetic data — a good model
for how to package and present your own study work.
<https://github.com/kousha1234/Research-portfolio>

### kshptl/kshptl.github.io · JavaScript
A data-scientist portfolio website. Reference for communicating your RWE work to
a broader audience.
<https://github.com/kshptl/kshptl.github.io>

### QuartzSoftwareLLC/quarry · HTML
Data insight and visualization dashboard. General-purpose viz tooling that can
front an RWE analysis.
<https://github.com/QuartzSoftwareLLC/quarry>

---

## Tagged but off-topic

### baali-who/rwaise · Python
"Real-World Asset Issuance & Settlement Engine for the XRP Ledger." This is a
**blockchain** project — "RWA/RWE" here means *real-world assets*, not real-world
evidence. It shares the tag by coincidence; **skip it** for RWE learning.
<https://github.com/baali-who/rwaise>

---

*The `rwe` topic evolves. If you find a new repo worth adding, follow
[CONTRIBUTING.md](../CONTRIBUTING.md).*

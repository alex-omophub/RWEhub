# 01 · The 4-Week Intern Learning Path

A structured curriculum. Each week has **learn → do → checkpoint**. Interns
should open a personal repo/notebook and commit their work at each checkpoint.

Prerequisites: comfort with either **R** or **Python**, basic statistics, and a
GitHub account.

---

## Week 1 — Foundations & Data Engineering

**Learn**
- Read [00-what-is-rwe.md](00-what-is-rwe.md) and the [glossary](03-glossary.md).
- Understand RWD sources and why the OMOP CDM exists.

**Do**
- Clone [`databricks-industry-solutions/omop-cdm`](https://github.com/databricks-industry-solutions/omop-cdm)
  and walk through how raw data lands in the CDM tables (`person`,
  `condition_occurrence`, `drug_exposure`, `observation_period`).
- Optional infra: [`eyedress02/modern-lakehouse`](https://github.com/eyedress02/modern-lakehouse)
  (MinIO + MariaDB + Dremio) or the claims path in
  [`ericg1212/healthcare-claims-pipeline`](https://github.com/ericg1212/healthcare-claims-pipeline)
  (FHIR → OMOP).

**✅ Checkpoint 1** — Write a one-page note: name 5 OMOP CDM tables, describe
what a "cohort" is, and diagram how one RWD source becomes CDM rows.

---

## Week 2 — Reproducibility & the Study Lifecycle

**Learn**
- Why RWE must be auditable: pre-registration, version control, environment
  locking, and audit reports.

**Do**
- Complete [`janickweberpals/icpe-git-2024`](https://github.com/janickweberpals/icpe-git-2024)
  ("Let's git it started") — git workflows across the RWE study lifecycle.
- Skim [`janickweberpals/agentic-code-review-ispe-2026`](https://github.com/janickweberpals/agentic-code-review-ispe-2026)
  for how code review scales quality.

**✅ Checkpoint 2** — Initialize your own study repo with a README, a locked
environment (`renv::init()` in R or a `requirements.txt`/`uv` lock in Python),
and a clean commit history.

---

## Week 3 — Statistical Methods & Causal Inference

**Learn**
- Confounding and the estimators that address it:
  - **Propensity score (PS) matching**
  - **IPTW** (inverse probability of treatment weighting)
  - **Cox proportional hazards** models
  - **Kaplan–Meier** survival curves
- The **target trial emulation** framework.

**Do**
- Run [`repro-stats/reproducr-rwe`](https://github.com/repro-stats/reproducr-rwe)
  end-to-end — it chains PS matching → IPTW → Cox PH → KM with `renv` locking and
  produces an academic audit report. This is the reference implementation.
- Study the course materials in
  [`al8xi8/EPID708_UMich2025`](https://github.com/al8xi8/EPID708_UMich2025)
  (ML for epidemiologic analysis, causal focus).

**✅ Checkpoint 3** — On a simulated/synthetic dataset, estimate a treatment
effect two ways (PS matching and IPTW), plot KM curves by arm, and interpret the
hazard ratio with its confidence interval.

---

## Week 4 — Apply: Reproduce & Propose

**Learn**
- How a domain study is framed, from question to endpoint.

**Do**
- Explore an applied study end-to-end:
  - [`htlin222/roche-vabysmo-rwe-workshop`](https://github.com/htlin222/roche-vabysmo-rwe-workshop)
    — interactive RWE analysis textbook (R + AI).
  - [`Krashnika-Deivakumar/aml-flt3-market-sizing`](https://github.com/Krashnika-Deivakumar/aml-flt3-market-sizing)
    — RWD simulation, market sizing, survival analysis.
  - [`natsousa/rwbiomarker`](https://github.com/natsousa/rwbiomarker) — biomarker
    analysis in colon cancer.
- Present results like a professional: model
  [`kousha1234/Research-portfolio`](https://github.com/kousha1234/Research-portfolio)
  and [`kshptl/kshptl.github.io`](https://github.com/kshptl/kshptl.github.io).

**✅ Checkpoint 4 (capstone)** — Pick a project from
[04-internship-projects.md](04-internship-projects.md), write a short protocol
(question, cohort, exposure, outcome, analysis, biases), and deliver a
reproducible mini-study with an R Markdown / Quarto or Jupyter report.

---

## Skills checklist

By the end of the program an intern should be able to:

- [ ] Explain RWD vs. RWE and name the major data sources
- [ ] Navigate an OMOP CDM schema and define a cohort
- [ ] Run a fully reproducible analysis (version control + locked environment)
- [ ] Apply PS matching / IPTW to control confounding
- [ ] Fit and interpret Cox PH models and Kaplan–Meier curves
- [ ] Frame a study as a target-trial emulation
- [ ] Communicate findings in an auditable, well-documented report

# 03 · Glossary

Key terms an RWE intern will meet in the first month.

## Data & infrastructure

- **RWD (Real-World Data)** — health data collected outside controlled trials
  (EHR, claims, registries, PRO, wearables).
- **RWE (Real-World Evidence)** — clinical evidence about a product's use,
  benefit, or risk derived from analyzing RWD.
- **OMOP CDM (Observational Medical Outcomes Partnership Common Data Model)** — a
  standardized schema + vocabularies that make observational data portable across
  databases. Stewarded by OHDSI.
- **OHDSI (Observational Health Data Sciences and Informatics)** — the open
  community behind the OMOP CDM and its tools (ATLAS, Achilles, HADES).
- **FHIR (Fast Healthcare Interoperability Resources)** — HL7 standard for
  exchanging healthcare data; a common ingestion source into the OMOP CDM.
- **Claims data** — billing records from payers; broad coverage, but codes are
  proxies for clinical truth.
- **EHR (Electronic Health Record)** — clinical records from care delivery.
- **Cohort** — a set of patients meeting defined entry/inclusion criteria over a
  time window.
- **Data lakehouse** — architecture combining a data lake's flexibility with a
  warehouse's structure (e.g., Databricks, or MinIO + Dremio).

## Study design

- **Target trial emulation** — designing an observational study to mimic the
  randomized trial you'd ideally run; the current best-practice framework.
- **Index date** — the time zero when a patient enters the study (e.g., first
  treatment).
- **Exposure / outcome** — the treatment being studied and the event being
  measured.
- **External control arm** — using RWD patients as the comparator for a
  single-arm trial.

## Biases

- **Confounding** — a variable affecting both treatment choice and outcome,
  distorting the estimated effect.
- **Immortal-time bias** — a span of follow-up during which the outcome cannot
  occur by design, biasing survival estimates.
- **Selection bias** — systematic differences in who is included/observed.
- **Misclassification** — errors in measuring exposure/outcome (codes ≠ truth).

## Statistical methods

- **Propensity Score (PS)** — the modeled probability of receiving treatment
  given covariates; used to balance groups.
- **PS matching** — pairing treated and untreated patients with similar PS.
- **IPTW (Inverse Probability of Treatment Weighting)** — weighting patients by
  the inverse of their treatment probability to create a pseudo-randomized
  sample.
- **Cox proportional hazards model** — regression for time-to-event data;
  produces a **hazard ratio (HR)**.
- **Hazard ratio (HR)** — relative rate of an event between groups over time; HR
  < 1 favors the treatment.
- **Kaplan–Meier (KM) curve** — nonparametric estimate of survival probability
  over time.
- **Confidence interval (CI)** — the plausible range for an estimate;
  non-overlap with the null (e.g., HR = 1) suggests statistical significance.

## Reproducibility & tooling

- **renv** — R package for locking a project's exact package versions.
- **R Markdown / Quarto** — literate-programming formats mixing code, results,
  and narrative into a reproducible report.
- **Audit report** — a generated document tracing every analytic step for review.
- **Agentic code review** — using AI agents to systematically check analysis code
  for errors and reproducibility issues.

## Regulatory / commercial

- **FDA / EMA** — U.S. and European medicines regulators; both accept
  well-designed RWE.
- **HEOR (Health Economics and Outcomes Research)** — using RWE to demonstrate
  value, inform pricing, and support market access.
- **Market sizing** — estimating the patient population and commercial
  opportunity for a therapy, often from RWD.

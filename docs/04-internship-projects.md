# 04 · Internship Capstone Projects

Starter projects for the Week 4 capstone. Each is scoped to be doable on
**public or synthetic data** so no protected health information is required.
Pick one, write a short protocol first, then build a reproducible mini-study.

## Project ideas

### P1 — Reproduce and extend a reference pipeline
Fork [`repro-stats/reproducr-rwe`](https://github.com/repro-stats/reproducr-rwe),
reproduce its PS-matching + Cox result, then add **one** extension: an IPTW
sensitivity analysis, a subgroup, or a negative-control outcome. Report whether
your conclusion is robust.

### P2 — OMOP cohort from scratch
Using a public OMOP dataset (e.g., the OHDSI synthetic Eunomia dataset), define a
cohort with clear inclusion/exclusion criteria and describe it (Table 1). Bonus:
compute an incidence rate for an outcome.

### P3 — Claims → CDM mini-ETL
Take a small FHIR/claims sample (see
[`ericg1212/healthcare-claims-pipeline`](https://github.com/ericg1212/healthcare-claims-pipeline))
and map a slice of it into OMOP CDM tables. Document every mapping decision.

### P4 — Survival analysis case study
On simulated data (model after
[`Krashnika-Deivakumar/aml-flt3-market-sizing`](https://github.com/Krashnika-Deivakumar/aml-flt3-market-sizing)
or [`natsousa/rwbiomarker`](https://github.com/natsousa/rwbiomarker)), compare two
arms with Kaplan–Meier curves and a Cox model. Interpret the HR and CI.

### P5 — Target trial emulation write-up
Choose a published RWE study and re-express its design as a target-trial
emulation: state the eligibility, treatment strategies, assignment, outcome, and
causal contrast. Identify the biggest threat to validity.

## Protocol template (write this first)

```
Title:
Question (PICO):   Population / Intervention / Comparator / Outcome
Data source:       (dataset, time window, OMOP or other)
Cohort definition: inclusion, exclusion, index date
Exposure:
Outcome:           definition + measurement window
Analysis:          estimator (PS matching / IPTW), model (Cox / KM)
Key biases:        confounders, immortal-time risk, missingness — and mitigations
Reproducibility:   repo layout, environment lock, how to re-run
```

## Deliverables

1. A public GitHub repo (fork or new) with a clear README.
2. A **locked environment** (`renv.lock` or `requirements.txt`/lockfile).
3. A reproducible report (R Markdown / Quarto or Jupyter) that runs top-to-bottom.
4. A 10-minute presentation of question → method → result → limitations.

## Evaluation rubric

| Dimension | What "excellent" looks like |
|-----------|-----------------------------|
| **Reproducibility** | A reviewer can clone and re-run to the same result |
| **Study design** | Clear PICO; threats to validity named and addressed |
| **Methods** | Estimator matches the question; results correctly interpreted |
| **Data handling** | Cohort logic and transformations documented |
| **Communication** | README + report + talk are clear to a non-expert |

---

Back to the [learning path](01-learning-path.md) · [hub home](../README.md)

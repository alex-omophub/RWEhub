# RWEhub 🧬📊

**A curated tutorial hub for Real-World Evidence (RWE), built for the CABS RWE Internship Program.**

RWEhub is a teaching companion that summarizes and organizes the open-source
projects tagged under GitHub's [`rwe` topic](https://github.com/topics/rwe).
Instead of a flat list of stars, it groups the ecosystem into a **guided learning
path** so an intern with a stats/programming background can go from "What is
real-world evidence?" to running a reproducible RWE study of their own.

> **Who this is for:** CABS RWE interns, new analysts, and anyone learning
> pharmacoepidemiology, OMOP/CDM data engineering, and causal inference on
> real-world healthcare data.

---

## What is Real-World Evidence (RWE)?

**Real-World Data (RWD)** is health data collected outside of randomized
controlled trials — from electronic health records (EHR), insurance claims,
disease registries, patient-reported outcomes, and wearables.

**Real-World Evidence (RWE)** is the clinical evidence about the use, benefits,
and risks of a medical product *derived from analyzing RWD*. Regulators (FDA,
EMA) increasingly accept well-designed RWE to support approvals, label
expansions, and post-market safety.

A modern RWE study almost always involves four skills, which map to the four
tracks in this hub:

| Skill | Question it answers | Track |
|-------|--------------------|-------|
| **Data engineering** | How do I turn messy EHR/claims data into an analyzable format? | [Track 1: Data & OMOP CDM](#track-1--data--omop-cdm) |
| **Reproducibility** | How do I make my study auditable and repeatable? | [Track 2: Reproducibility & Study Lifecycle](#track-2--reproducibility--study-lifecycle) |
| **Causal inference** | How do I estimate a treatment effect without a randomized trial? | [Track 3: Methods & Causal Inference](#track-3--methods--causal-inference) |
| **Application** | What does a real end-to-end study look like? | [Track 4: Applied Case Studies](#track-4--applied-case-studies) |

---

## 🗺️ The 4-Week Intern Learning Path

Each week pairs a concept with a hands-on repository to clone and run.

### Week 1 — Foundations & Data
Understand RWD sources and the **OMOP Common Data Model (CDM)**, the standard
that lets studies be portable across databases.
- Read: [What is RWE](docs/00-what-is-rwe.md) · [Glossary](docs/03-glossary.md)
- Do: Stand up a lakehouse and explore an OMOP schema — `databricks-industry-solutions/omop-cdm`, `eyedress02/modern-lakehouse`

### Week 2 — Reproducibility
Learn version control, environment locking (`renv`), and audit reporting so your
work survives peer and regulatory scrutiny.
- Do: Work through `janickweberpals/icpe-git-2024` (git for the RWE lifecycle)

### Week 3 — Methods
Propensity score matching, IPTW, Cox proportional hazards, Kaplan–Meier survival,
and causal inference.
- Do: Run the end-to-end pipeline in `repro-stats/reproducr-rwe`; study `al8xi8/EPID708_UMich2025`

### Week 4 — Apply
Reproduce a domain study and start your own mini-project.
- Do: Explore `htlin222/roche-vabysmo-rwe-workshop`, `Krashnika-Deivakumar/aml-flt3-market-sizing`, `natsousa/rwbiomarker`
- Then: Pick an [Internship Project](docs/04-internship-projects.md)

Full curriculum with checkpoints → **[docs/01-learning-path.md](docs/01-learning-path.md)**

---

## 📚 Curated Repository Catalog

The 15 repositories from the `rwe` topic, grouped by what they teach.
Full annotations in **[docs/02-curated-repos.md](docs/02-curated-repos.md)**.

### Track 1 — Data & OMOP CDM
Turning raw health data into standardized, analyzable tables.

| Repo | Lang | What you'll learn |
|------|------|-------------------|
| [databricks-industry-solutions/omop-cdm](https://github.com/databricks-industry-solutions/omop-cdm) | Python | Building an OMOP CDM on a modern data lakehouse ⭐ *start here* |
| [eyedress02/modern-lakehouse](https://github.com/eyedress02/modern-lakehouse) | Shell | Lakehouse stack with MinIO, MariaDB, Dremio |
| [ericg1212/healthcare-claims-pipeline](https://github.com/ericg1212/healthcare-claims-pipeline) | Python | HL7 FHIR → OMOP CDM, claims classification, cohort building |
| [aminyakubu/explorys](https://github.com/aminyakubu/explorys) | R | Pulling cohort demographics from the IBM Explorys database |

### Track 2 — Reproducibility & Study Lifecycle
Making studies transparent, auditable, and repeatable.

| Repo | Lang | What you'll learn |
|------|------|-------------------|
| [janickweberpals/icpe-git-2024](https://github.com/janickweberpals/icpe-git-2024) | HTML | Git + transparency across the RWE study lifecycle ⭐ *start here* |
| [repro-stats/reproducr-rwe](https://github.com/repro-stats/reproducr-rwe) | R | Full reproducible pipeline: PS matching, IPTW, Cox, KM, `renv`, audit report |
| [janickweberpals/agentic-code-review-ispe-2026](https://github.com/janickweberpals/agentic-code-review-ispe-2026) | R | Using AI agents to review analytics code |

### Track 3 — Methods & Causal Inference
The statistics that make RWE credible.

| Repo | Lang | What you'll learn |
|------|------|-------------------|
| [al8xi8/EPID708_UMich2025](https://github.com/al8xi8/EPID708_UMich2025) | R | Machine learning + causal inference for epidemiology (course) |
| [htlin222/roche-vabysmo-rwe-workshop](https://github.com/htlin222/roche-vabysmo-rwe-workshop) | R | Interactive textbook: clinical RWE analysis with R + AI |

### Track 4 — Applied Case Studies & Portfolios
End-to-end and domain-specific examples to model your own work on.

| Repo | Lang | What you'll learn |
|------|------|-------------------|
| [Krashnika-Deivakumar/aml-flt3-market-sizing](https://github.com/Krashnika-Deivakumar/aml-flt3-market-sizing) | R | RWD simulation for AML market sizing + survival analysis |
| [natsousa/rwbiomarker](https://github.com/natsousa/rwbiomarker) | R | RWE biomarker analysis in colon cancer |
| [kousha1234/Research-portfolio](https://github.com/kousha1234/Research-portfolio) | R | R Markdown research portfolio on synthetic data |
| [kshptl/kshptl.github.io](https://github.com/kshptl/kshptl.github.io) | JS | Data-scientist portfolio site (presenting your work) |
| [QuartzSoftwareLLC/quarry](https://github.com/QuartzSoftwareLLC/quarry) | HTML | Data insight & visualization dashboard |

> ℹ️ `baali-who/rwaise` also carries the `rwe` tag but is a blockchain
> ("Real-World Asset") project — **not** real-world evidence. Included for
> completeness; skip it for RWE learning.

---

## 🚀 Quick Start for Interns

```bash
# 1. Clone this hub
git clone https://github.com/cabsweb/RWEhub.git
cd RWEhub

# 2. Read the orientation docs
open docs/00-what-is-rwe.md
open docs/01-learning-path.md

# 3. Follow Week 1 — clone your first data repo
git clone https://github.com/databricks-industry-solutions/omop-cdm.git
```

## 🗂️ Repository Contents

```
RWEhub/
├── README.md                     # You are here
├── docs/
│   ├── 00-what-is-rwe.md          # RWE/RWD concepts & data sources
│   ├── 01-learning-path.md        # Detailed 4-week curriculum + checkpoints
│   ├── 02-curated-repos.md        # Full annotations for all 15 repos
│   ├── 03-glossary.md             # OMOP, IPTW, Cox PH, FHIR, ... defined
│   └── 04-internship-projects.md  # Starter project ideas + rubric
├── CONTRIBUTING.md                # How interns add repos & fix docs
└── LICENSE
```

## 🤝 Contributing

Interns are encouraged to keep this hub current. Found a new RWE repo, or a
better explanation? See **[CONTRIBUTING.md](CONTRIBUTING.md)**.

---

*Maintained by the CABS RWE Internship Program · Source topic: <https://github.com/topics/rwe>*

<!-- RWEhub · CABS RWE Internship Program -->

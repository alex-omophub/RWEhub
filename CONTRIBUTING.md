# Contributing to RWEhub

RWEhub is a living teaching resource for the CABS RWE Internship Program.
Interns and mentors are encouraged to keep it current.

## Ways to contribute

- **Add a repo** — found a new project under the
  [`rwe` topic](https://github.com/topics/rwe) (or elsewhere) worth learning
  from? Add it.
- **Improve an annotation** — sharpen a description or fix a stale star count.
- **Fix or extend docs** — clearer explanations, new glossary terms, better
  project ideas.

## How to add a repository

1. Decide which track it belongs to (Data & CDM, Reproducibility, Methods, or
   Applied Case Studies).
2. Add a row to the matching table in [`README.md`](README.md).
3. Add a full annotation in [`docs/02-curated-repos.md`](docs/02-curated-repos.md)
   with: full name, language, one-line description, and *what an intern learns
   from it*.
4. If a repo carries the `rwe` tag but isn't about real-world **evidence** (e.g.,
   real-world **assets**/blockchain), put it under "Tagged but off-topic" and say
   why.

## Style

- Keep annotations to 1–3 sentences, focused on the learning value.
- Link to repos with full `https://github.com/owner/repo` URLs.
- Prefer plain language; define jargon in [`docs/03-glossary.md`](docs/03-glossary.md).

## Workflow

```bash
git checkout -b add-<short-name>
# make edits
git commit -m "docs: add <repo> to Track N"
git push origin add-<short-name>
# open a pull request against main
```

A mentor will review and merge. Thanks for helping the next cohort learn faster!

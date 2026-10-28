# Changelog

## 2026-10-28 — merged edition

- Merged *Brain Data & Brain-Model Initiatives: History and Master List* and *Open Neuroscience Data Resources —
  Master List* into one site, history first.
- Removed duplicated descriptions for ~20 entities that appeared in both documents, following the split rule in
  [Methodology](methodology.md); every removal is listed in the deduplication log.
- Collapsed the internal duplicate in the history document, where the Brain Knowledge Platform was described both as
  its own section and as a row in the archives table.
- Added FRDR, the Open Brain Institute and the Korea Brain Bank Network to the resource list (185 → 188 resources).
- Made `data/neuroscience_data_resources.csv` the single source of truth: the 13 category pages are generated from it
  by `scripts/build_resource_pages.py`, and CI fails if they are stale.

## 2026-10-27 — source documents

- *Brain Data & Brain-Model Initiatives: History and Master List* compiled (33 initiatives).
- *Open Neuroscience Data Resources — Master List* compiled (185 resources, 13 categories).

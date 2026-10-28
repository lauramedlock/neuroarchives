# Methodology & scope

## What this site is made of

Two independently compiled documents, merged in October 2026:

1. **Brain Data & Brain-Model Initiatives: History and Master List** — a narrative history of ~33 initiatives with
   dates, budgets, status and outlook. It became the [History](../history/index.md) section.
2. **Open Neuroscience Data Resources — Master List** — 185 resources in 13 categories with host, region, species,
   technique, biological level, access terms and URL, plus a machine-readable CSV and a species-by-level coverage
   figure. It became the [Resource list](../resources/index.md).

The history precedes the resource list because it explains why the inventory has the shape it does — why the archive
layer is crowded and durable, why mouse and human dominate, and why the model-oriented categories are thin.

## The rule used to remove duplicates

Roughly twenty entities appeared in both documents. Rather than deleting one copy, each fact was assigned to exactly
one half of the site:

- **History keeps** founding year, founders, funding amounts, programme lineage (what superseded what) and current
  funding status.
- **The resource list keeps** what the resource holds, species, technique, biological level, access conditions and
  the URL.

The clearest case is the history document's *Data archives, standards and infrastructure* table: 15 of its 16 rows
described resources that already had fuller entries in the resource list. That table is now a
[timeline-and-status table](../history/infrastructure.md) whose descriptive column was reduced to historical origin
only, with a link to the full entry. Nothing was lost; it is stated once.

## Deduplication log

| Entity | Appeared as | Full entry in resource list | Treatment |
|---|---|---|---|
| **INCF** | Archives table row | [INCF Training Space & standards portal](../resources/standards-catalogs.md) | Description dropped; founding (7 OECD countries, 2005) and status kept |
| **BIDS** | Archives table row | [Brain Imaging Data Structure (BIDS)](../resources/standards-catalogs.md) | Description dropped; publication year and extension history kept |
| **NWB** | Archives table row | [Neurodata Without Borders (NWB)](../resources/standards-catalogs.md) | Description dropped; founders (Kavli, Allen, LBNL) and version dates kept |
| **OpenNeuro** | Archives table row | [OpenNeuro](../resources/federated-archives.md) | Description dropped; OpenfMRI lineage and BRAIN designation kept |
| **DANDI** | Archives table row | [DANDI Archive](../resources/federated-archives.md) | Description dropped; funders and holdings-growth status kept |
| **NeMO, BIL, DABI, BossDB, EMBER** | Archives table row (5 bulleted expansions) | [5 separate entries](../resources/federated-archives.md) | All five bulleted descriptions dropped — each is a fuller entry in the resource list; the one-archive-per-data-type policy point kept |
| **EBRAINS** | Archives table row + national section | [EBRAINS Data & Knowledge Services; EBRAINS Model Catalog](../resources/federated-archives.md) | Service inventory dropped from the table; HBP-legacy origin and funding status kept in both |
| **Brain Knowledge Platform** | Archives table row *and* its own history section (internal duplicate) | [Brain Knowledge Platform / BCDC](../resources/reference-atlases.md) | The two near-identical history passages collapsed into one; tool inventory dropped |
| **CONP** | Archives table row + Canada section | [Canadian Open Neuroscience Platform (CONP)](../resources/federated-archives.md) | Kept once in the history table; the Canada section now cross-links instead of describing |
| **UK Biobank imaging** | Archives table row + wave-2 narrative | [UK Biobank Imaging](../resources/human-neuroimaging.md) | Description dropped; scan-milestone and repeat-scan status kept |
| **ENIGMA Consortium** | Archives table row | [ENIGMA Consortium](../resources/human-neuroimaging.md) | Description dropped; founding year and network size kept |
| **International Brain Laboratory** | Archives table row + foundation-model table | [International Brain Laboratory (IBL) data portal](../resources/neurophysiology.md) | Kept in both, but as different facts: 2017 founding in the table, brain-wide map as training data in the foundation-model section |
| **ModelDB** | Archives table row | [ModelDB](../resources/models.md) | Description dropped; 1996 SenseLab origin and model count kept |
| **NeuroMorpho.Org** | Archives table row | [NeuroMorpho.Org](../resources/connectomics.md) | Description dropped; 2006 start and reconstruction count kept |
| **Open Source Brain / NeuroML** | Archives table row | [Open Source Brain; NeuroML Database](../resources/models.md) | Description dropped; NeuroML-then-OSB sequence kept |
| **MICrONS** | History section + foundation-model table | [MICrONS Explorer](../resources/connectomics.md) | Kept: the program history and the digital-twin model are distinct facts; both now link to the dataset entry |
| **SuperAnimal / DeepLabCut** | Foundation-model table | [DeepLabCut Model Zoo & benchmarks](../resources/behavior.md) | Kept in the foundation-model table (that is the page's subject); now cross-linked rather than re-described |
| **Blue Brain Project** | History section + simulation route | [Blue Brain Project open data & portals](../resources/models.md) | Kept; closure and successor are history, the downloadable models are the resource entry |

## Resources merged in from the history document

Three resources were described in the history document but had no entry in the resource list. They were added to the
CSV, with their metadata derived from the history document rather than from an independent check of the host site:

| Resource | Added to category |
|---|---|
| [Federated Research Data Repository (FRDR)](../resources/federated-archives.md) | Federated archives & multi-modal repositories |
| [Open Brain Institute](../resources/models.md) | Computational models, simulation & benchmarks |
| [Korea Brain Bank Network](../resources/disease-genetics.md) | Disease, genetics & biobank portals |

This brings the count from 185 to **188**. The coverage figure was computed on the original 185 and was not
recomputed, so it does not include these three; the figure caption says so.

## Limitations carried over from the sources

- URLs and access conditions were not re-verified against live sites at compile time. Treat a dead link as a portal
  reorganization to look up, not a retired resource.
- Dataset sizes and holdings are the figures reported at the latest release known to the compilation; consortium
  holdings grow continuously.
- Some background facts in the history (founding dates of the HCP, the Allen atlases, FlyWire and the US Human Brain
  Project) come from general knowledge rather than a page opened for the review.
- Status fields reflect public information as of October 2026.

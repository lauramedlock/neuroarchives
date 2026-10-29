# NeuroArchives: A Field Guide to Neuro Data & Resources

*Created October 2026 · @Laura M*

If you're starting a project with a tight budget, looking for experimental data to model/analyze, or needing a comparison cohort: **the data you need probably already exist and this guide will help you find it.** 

The scale of data that is already publicly available is easy to underestimate. Every synapse in a fruit fly's brain (all 140,000
neurons and roughly 50 million connections) has been reconstructed and published. So has a cubic millimetre of mouse
visual cortex in which 200,000 cells each come with a recording of what they did while the animal watched a movie.
Brain scans from 100,000 people. Gene expression for all 302 neurons of a nematode, measured one neuron at a time.

The hard part is that this data sits in many separate portals, 
each with its own login, licence, file format, and vocabulary.

**This site is the map.**

<div class="grid cards" markdown>

-   :material-timeline-clock: **[Part I — History](history/index.md)**

    ---

    A short overview of how the open neuroscience data field has evolved: four waves from 1990s neuroinformatics to
    today's brain foundation models, the national initiatives behind them, and what remains funded as of October 2026.

    [:octicons-arrow-right-24: Read the history](history/index.md)

-   :material-database-search: **[Part II — Resource List](resources/index.md)**

    ---

    Where that data lives and how to access it: archives, atlases, cohorts and benchmarks across different categories,
    each with host, species, technique, biological level and access terms.

    [:octicons-arrow-right-24: Browse the resource list](resources/index.md)

</div>

## Finding your resource

```mermaid
%%{init: {"flowchart": {"curve": "stepBefore", "nodeSpacing": 35, "rankSpacing": 55, "useMaxWidth": false}} }%%
flowchart TD
    START([What do you need?])
    START --> EXP[Experimental data]
    START --> MOD[Computational models<br>and tools]

    EXP --> PREP{Preparation}
    PREP -->|Human, in vivo| HU{Modality}
    PREP -->|Human, post-mortem<br>or iPSC-derived| HPM{Measurement}
    PREP -->|Rodent or<br>nonhuman primate| RO{Modality}
    PREP -->|Fly, worm,<br>zebrafish| INV{Modality}
    PREP -->|Undecided —<br>search broadly first| FED[Federated archives]

    HU -->|MRI, fMRI, dMRI, PET| E1[Neuroimaging cohorts]
    HU -->|EEG, MEG, iEEG| E2[Human electrophysiology]

    HPM -->|Tissue, genotypes,<br>disease cohorts| E3[Disease, genetics<br>and biobanks]
    HPM -->|Organoid and<br>culture recordings| E4[Organoids and<br>in-vitro models]

    RO -->|Spiking, LFP,<br>calcium imaging| E5[Neurophysiology]
    RO -->|EM, tracing,<br>morphology| E6[Connectomics]
    RO -->|scRNA-seq, snATAC,<br>spatial omics| E7[Transcriptomics]
    RO -->|Video and<br>pose tracking| E8[Behaviour and pose]

    INV -->|Wiring| E6
    INV -->|Expression| E7
    INV -->|Genes, alleles,<br>anatomy ontologies| E9[Model-organism<br>knowledgebases]

    MOD --> PURPOSE{Purpose}
    PURPOSE -->|Register my data into<br>a common coordinate space| M1[Reference atlases and<br>coordinate frameworks]
    PURPOSE -->|Simulate circuits,<br>reuse published models| M2[Models, simulation<br>and benchmarks]
    PURPOSE -->|Score a model<br>against neural data| M2
    PURPOSE -->|Convert formats, find<br>repositories, cite RRIDs| M3[Standards, tooling<br>and catalogs]
```
Now explore the matching dataset/resource:

### Experimental data

<div class="grid cards" markdown>

-   **Human, in vivo**

    [Neuroimaging cohorts and population studies](resources/human-neuroimaging.md) ·
    [EEG, MEG and iEEG](resources/human-electrophysiology.md)

-   **Human, post-mortem and in vitro**

    [Disease, genetics and biobank portals](resources/disease-genetics.md) ·
    [Organoids, stem cells and in-vitro models](resources/organoids.md)

-   **Rodent and nonhuman primate**

    [Neurophysiology and neural activity](resources/neurophysiology.md) ·
    [Connectomics and morphology](resources/connectomics.md) ·
    [Transcriptomics and spatial omics](resources/transcriptomics.md) ·
    [Behaviour, video and pose](resources/behavior.md)

-   **Invertebrate and small vertebrate**

    [Connectomics](resources/connectomics.md) · [Transcriptomics](resources/transcriptomics.md) ·
    [Model-organism knowledgebases](resources/model-organisms.md)

</div>

### Models and tools

<div class="grid cards" markdown>

-   **Simulation and benchmarking**

    [Computational models, simulation, and benchmarks](resources/models.md) — published model source, whole-brain
    simulators, and benchmarks that score models against neural recordings.

-   **Formats, converters, and registries**

    [Standards, tooling and resource catalogs](resources/standards-catalogs.md) — BIDS, NWB, DataLad, and the
    registries to search when this list runs out.

</div>

## State of the Field

- **Open data sharing is working.** Open archives (OpenNeuro, DANDI, EBRAINS) and the shared formats beneath
  them (BIDS for imaging, NWB for neurophysiology) are active and growing, and now also serve as the training substrate
  for pooled models of neural activity.
- **Megaprojects have converted into permanent infrastructure.** The EU Human Brain Project ended in 2023 and was
  succeeded by EBRAINS; Blue Brain closed in 2024 and its assets moved to the Open Brain Institute; Japan's Brain/MINDS
  became Brain/MINDS 2.0.
- **Funding is shifting.** US BRAIN funding sits below its 2023 peak and its 21st Century Cures Act component ends
  after FY2026, while China and Japan are expanding. Canada and Australia have mature national strategies without
  dedicated national budgets.

## Two halves, two questions

Plenty of things appear in both parts of this site... EBRAINS is simultaneously a 2019 EU initiative and an archive you
can download data from. Nothing is described twice; which half you want depends on your question:

| Your question | Where it is answered |
|---|---|
| When did it start, who paid for it, is it still funded? | [History](history/index.md) |
| What does it hold, for which species, and how do I get in? | [Resource list](resources/index.md) |

## Before you download anything

Check the **Access** column first. Four tiers show up across the list: *fully open* (click and download), *registration* (free account), *data-use agreement* (a signature, no
review), and *controlled access* (committee review, often weeks, sometimes an institutional signing official).

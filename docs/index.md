# NeuroArchives: A Field Guide to Neuro Data & Resources

*Created October 2026 · @Laura M*

If you're starting a project with a tight budget, looking for experimental data to model/analyze, or needing a comparison cohort: **the data you need probably already exist and this guide will help you find it.** 

The scale of data that is already publicly available is easy to underestimate. Every synapse in a fruit fly's brain (all 140,000
neurons and roughly 50 million connections) has been reconstructed and published. So has a cubic millimetre of mouse
visual cortex in which 200,000 cells each come with a recording of what they did while the animal watched a movie.
Brain scans from 100,000 people. Gene expression for all 302 neurons of a nematode, measured one neuron at a time.

The hard part is that this data sits in many separate portals, 
each with its own login, licence, file format, and vocabulary.

## **This site is the map.**

<div class="grid cards" markdown>

-   :material-timeline-clock: **[Part I — History](history/index.md)**

    ---

    A short overview of how the open neuroscience data field has evolved: four waves from 1990s neuroinformatics to
    today's brain foundation models, the national initiatives behind them, and what remains funded.

    [:octicons-arrow-right-24: Read the history](history/index.md)

-   :material-database-search: **[Part II — Resource List](resources/index.md)**

    ---

    Where that data lives and how to access it: archives, atlases, cohorts and benchmarks across different categories,
    each with host, species, technique, biological level and access terms.

    [:octicons-arrow-right-24: Browse the resource list](resources/index.md)

</div>

## Finding your resource

```mermaid
%%{init: {"flowchart": {"curve": "stepBefore", "nodeSpacing": 35, "rankSpacing": 55, "useMaxWidth": true}} }%%
flowchart LR
    START([What Do You Need?])
    START --> EXP[Experimental Data]
    START --> MOD[Computational Models<br>and Tools]

    EXP --> PREP([Preparation])
    PREP -->|Human| HU([Modality])
    PREP -->|Rodent or<br>NHP| RO([Modality])
    PREP -->|Fly, Worm,<br>Zebrafish| INV([Modality])
    PREP -->|Undecided| GEN([Modality])

    HU -->|MRI, fMRI, dMRI, PET| E1[Neuroimaging]
    HU -->|EEG, MEG, iEEG| E2[Electrophysiology]
    HU -->|Tissue, Genotypes,<br>Disease Cohorts| E3[Disease, Genetics,<br>& Biobanks]
    HU -->|Organoid and<br>Culture Recordings| E4[Organoids & Stem Cells]

    RO -->|Spiking, LFP,<br>Ca2+ Imaging| E5[Neurophysiology] 
    RO -->|EM, Tracing,<br>Morphology| E6[Connectomics, <br> Morphology]
    RO -->|scRNA-seq, snATAC,<br>spatial-omics| E7[Transcriptomics]
    RO -->|Video and<br>Pose Tracking| E8[Behaviour and Pose]

    INV -->|Wiring| E6
    INV -->|Expression| E7
    INV -->|Genes, Alleles,<br>Anatomy Ontologies| E9[Model-Organism<br>Databases]

    GEN -->|General Archives| E10[Multi-Modal Repositories]

    MOD --> PURPOSE([Purpose])
    PURPOSE -->|Register my data into<br>a common coordinate space| M1[Reference Atlases and<br>Coordinate Frameworks]
    PURPOSE -->|Simulate circuits,<br>reuse published models| M2[Models, Simulation]
    PURPOSE -->|Score a model<br>against neural data| M4[Benchmarks]
    PURPOSE -->|Convert data formats, find<br>repositories, cite RRIDs| M3[Standards, Tools,<br>and Catalogs]
```

Now explore the matching dataset/resource:

### Experimental Data

<div class="grid cards" markdown>

-   **Human**

    [Neuroimaging](resources/human-neuroimaging.md) ·
    [Electrophysiology](resources/human-electrophysiology.md) ·
    [Disease, genetics, and biobank portals](resources/disease-genetics.md) ·
    [Organoids, stem cells, and in-vitro models](resources/organoids.md)

-   **Animal (rodent, NHP)**

    [Neurophysiology](resources/neurophysiology.md) ·
    [Connectomics and Morphology](resources/connectomics.md) ·
    [Transcriptomics and spatial -omics](resources/transcriptomics.md) ·
    [Behaviour and Pose Estimation](resources/behavior.md)

-   **Invertebrate and Small Vertebrate**

    [Connectomics](resources/connectomics.md) · [Transcriptomics](resources/transcriptomics.md) ·
    [Model-Organism Databases](resources/model-organisms.md)

-   **General-purpose archives**

    [Multi-modal Repositories](resources/federated-archives.md) — Federated, standards-based archives
    holding data from many labs. 

</div>

### Models and Tools

<div class="grid cards" markdown>

-   **Simulation and Benchmarking**

    [Computational Models & Simulation](resources/models.md) · [Benchmarking](resources/benchmarking.md)

-   **Formats, Converters, and Registries**

    [Standards, Tooling and Resource Catalogs](resources/standards-catalogs.md)

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

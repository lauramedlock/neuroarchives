# NeuroArchives: A Field Guide to Neuroscience Data & Resources

Source for a documentation site combining a history of brain-data and brain-model initiatives worldwide with a master
list of 188 open neuroscience data resources. Built with [MkDocs](https://www.mkdocs.org/) and
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/); publishes to Read the Docs, GitHub Pages, or both.

```
.
├── mkdocs.yml                     # site config and navigation
├── .readthedocs.yaml              # Read the Docs build config
├── requirements.txt               # pinned build dependencies
├── data/
│   ├── neuroscience_data_resources.csv   # SINGLE SOURCE OF TRUTH for the 188 resources
│   └── categories.json                   # category slugs, titles, intro paragraphs
├── scripts/
│   └── build_resource_pages.py    # CSV -> docs/resources/*.md
├── docs/
│   ├── index.md                   # landing page
│   ├── history/                   # hand-written history pages
│   ├── resources/                 # GENERATED category pages (do not edit by hand)
│   └── assets/                    # coverage figure, extra CSS
└── .github/workflows/docs.yml     # build, staleness check, GitHub Pages deploy
```

## Licence

Text and tables: CC BY 4.0, attributing the original compilations. The linked resources carry their own licences — the
**Access** column states the conditions for each.

# Brain Data & Brain-Model Initiatives

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
│   ├── about/                     # methodology, changelog, contributing
│   └── assets/                    # coverage figure, extra CSS
└── .github/workflows/docs.yml     # build, staleness check, GitHub Pages deploy
```

## Quick start

```bash
git clone https://github.com/USERNAME/brain-data-docs.git
cd brain-data-docs
python -m venv .venv && source .venv/bin/activate     # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python scripts/build_resource_pages.py                # regenerate resource pages from the CSV
mkdocs serve                                          # http://127.0.0.1:8000
```

`mkdocs build --strict` fails on any broken internal link, so run it before pushing.

## Publishing

### Step 1 — put it on GitHub

```bash
git init
git add .
git commit -m "Brain data history and resource list"
gh repo create brain-data-docs --public --source=. --push     # or create the repo in the web UI
```

Then replace `USERNAME` with your GitHub account in `mkdocs.yml` (`repo_url`, `repo_name`) and in
`docs/resources/index.md` (the CSV download link).

### Step 2a — Read the Docs

1. Sign in at [readthedocs.org](https://readthedocs.org) with GitHub and grant access to the repository.
2. **Add project** → import `brain-data-docs`. Read the Docs detects `.readthedocs.yaml` automatically; no build
   settings need changing.
3. The first build takes a couple of minutes and lands at `https://<project-slug>.readthedocs.io`.
4. Optional: in **Admin → Automation rules**, add a rule to activate and build every new tag, so tagged releases get
   their own versioned docs.

The config pins Python 3.12 and runs `scripts/build_resource_pages.py` in the `pre_build` job, so a CSV edit is enough
to change the published site.

### Step 2b — GitHub Pages

The included workflow deploys on every push to `main`.

1. Push once so the workflow runs and creates the `gh-pages` branch.
2. **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `gh-pages`, folder `/ (root)`.
3. The site appears at `https://USERNAME.github.io/brain-data-docs/`.

Running both is fine — the same `mkdocs.yml` drives each.

### Step 3 — custom domain (optional)

Add a `docs/CNAME` file containing the domain, point a CNAME DNS record at `USERNAME.github.io`, and set the domain
under **Settings → Pages**. On Read the Docs, use **Admin → Domains**.

## Editing

Resource entries live in the CSV, not in the generated pages — see
[docs/about/contributing.md](docs/about/contributing.md). History pages are ordinary markdown under `docs/history/`.

## Licence

Text and tables: CC BY 4.0, attributing the original compilations. The linked resources carry their own licences — the
**Access** column states the conditions for each.

# Contributing

## Adding or editing a resource

Resource pages are **generated** — editing `docs/resources/*.md` directly will be overwritten on the next build.

1. Edit `data/neuroscience_data_resources.csv`. One row per resource; columns are `Category, Resource, Host, Region,
   Species, Technique, Level, Description, URL, Access`. `Category` must match a title in `data/categories.json`
   exactly.
2. Regenerate the pages:

    ```bash
    python scripts/build_resource_pages.py
    ```

3. Preview locally with `mkdocs serve`, then commit both the CSV and the regenerated pages.

Conventions worth keeping: semicolon-separated lists in `Species`, `Technique` and `Level`; `Access` phrased as what
the user has to do (*Fully open*, *Free account*, *Data-use agreement*, *Application-based access*); `Description` two
to four sentences, stating what the resource holds rather than why it matters.

## Adding or renaming a category

Edit `data/categories.json` (`slug`, `title`, `intro`) and add the page to the `nav:` block in `mkdocs.yml`. The slug
becomes the filename.

## Editing the history

History pages are hand-written markdown in `docs/history/`. Before adding a description of what an archive or atlas
holds, check whether it belongs in the resource list instead — see the split rule in
[Methodology](methodology.md).

## Checks that run on every push

`.github/workflows/docs.yml` regenerates the resource pages, fails if the committed versions are stale, and builds
with `mkdocs build --strict` so that a broken internal link fails the build.

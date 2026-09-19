# Contributing to these docs

These docs are built with [Zensical](https://zensical.org) and published to
GitHub Pages automatically whenever a change is merged into `main`.

## Edit a page

Every page has an edit button that opens the source file on GitHub. Make your
change there and open a pull request. The build runs automatically on the
pull request, so broken pages are caught before merge.

## Work locally

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
zensical serve
```

Open <http://localhost:8000>. The preview reloads as you save.

## Add a page

1. Create a Markdown file under `docs/`, in the folder for its section.
2. Add it to `nav` in `zensical.toml`.
3. Run `zensical build --clean` to confirm it builds, then open a pull request.

!!! warning "Everything here is public"
    This site is published on the open internet. Don't commit client names,
    internal notes, or credentials, including in HTML comments or in files
    that aren't listed in the navigation. Zensical builds every Markdown file
    under `docs/`, whether or not it appears in `nav`.

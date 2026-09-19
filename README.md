# PraxisFive.github.io

Source for the PraxisFive documentation site, published at
<https://praxisfive.github.io>.

Built with [Zensical](https://zensical.org). See
[`docs/about/contributing.md`](docs/about/contributing.md) for how to edit,
preview, and add pages.

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
zensical serve            # preview at http://localhost:8000
zensical build --clean    # production build into site/
```

Pushes to `main` deploy automatically via `.github/workflows/docs.yml`.

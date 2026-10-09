<p align="center">
  <img src="CLAIM+logo+solid+blue.jpg" alt="CLAIM Logo" width="480" />
</p>

# CLAIM: Checklist for Artificial Intelligence in Medical Imaging — Explanation, Elaboration and Examples

This repository hosts the companion website for the **CLAIM 2024 Update** reporting guideline. The site provides a detailed explanation and elaboration of each of the 44 CLAIM checklist items, supplemented by illustrative examples from the literature demonstrating appropriate adherence to each item.

The objective is to support researchers and reviewers in the accurate and effective application of the CLAIM guideline by clarifying the intent and proper implementation of each item, reducing common misinterpretations, and encouraging effective use of the checklist.

## Website

🌐 **[https://rsna.github.io/claim/](https://rsna.github.io/claim/)**

The site includes:

- **CLAIM 2024 Checklist** — Interactive checklist table matching the official format, with fillable page/line fields, No and NA checkboxes, and a Print / Export PDF button. Each item links to its elaboration page.
- **CLAIM 2024 Items** — All 44 items grouped by section (Title/Abstract, Introduction, Methods, Results, Discussion, Other Information). Each item page contains the item definition, explanation and elaboration, and illustrative examples from the literature.
- **References** — Full reference list for all cited works.

## Citation

This website accompanies the following article. If you use this resource, please cite:

Akinci D'Antonoli T, Adams LC, Amyar A, et al. Checklist for Artificial Intelligence in Medical Imaging (CLAIM): Explanation, Elaboration, and Examples. *Radiol Artif Intell* 2026; 8:e260835. [https://doi.org/10.1148/ryai.260835](https://doi.org/10.1148/ryai.260835)

## Reference

Tejani AS, Klontzas ME, Gatti AA, et al. Checklist for Artificial Intelligence in Medical Imaging (CLAIM): 2024 Update. *Radiol Artif Intell* 2024; 6:e240300. [https://doi.org/10.1148/ryai.240300](https://doi.org/10.1148/ryai.240300)

## Links

- [CLAIM Guideline site](https://pubs.rsna.org/page/ai/claim)
- [CLAIM Explanation, Elaboration, and Examples article](https://doi.org/10.1148/ryai.260835)
- [CLAIM 2024 Update article](https://pubs.rsna.org/doi/10.1148/ryai.240300)

## Repository structure

```text
.
├── docs/                  # Jekyll documentation site (GitHub Pages source)
│   ├── _config.yml        # Site configuration
│   ├── _plugins/          # Ruby compatibility plugin
│   ├── _sass/custom/      # Custom CSS overrides
│   ├── _includes/         # Custom Jekyll includes (prev/next navigation)
│   ├── assets/            # Logo and figures
│   ├── index.md           # Home page
│   ├── checklist.md       # Interactive CLAIM 2024 Checklist
│   ├── claim-items.md     # Items overview (grouped by section)
│   ├── item-01.md … item-44.md  # Individual item pages
│   └── references.md      # References
├── .github/workflows/     # GitHub Pages deployment workflow
├── start.sh               # One-command local server + tunnel script
├── CITATION.cff           # Citation metadata
├── CONTRIBUTING.md        # Contribution guidance
├── LICENSE                # Content license (CC BY-NC-ND 4.0)
└── LICENSE-CODE           # Code license (MIT)
```

## Local preview

Requires Ruby 3.3 (install via Homebrew: `brew install ruby@3.3`).

```bash
cd docs
PATH="/usr/local/opt/ruby@3.3/bin:$PATH" GEM_HOME="$HOME/.gem/ruby/3.3.0" bundle install
PATH="/usr/local/opt/ruby@3.3/bin:$PATH" GEM_HOME="$HOME/.gem/ruby/3.3.0" bundle exec jekyll serve
```

The site will be available at `http://localhost:4000`.

Alternatively, use `./start.sh` from the repository root to start Jekyll and a Cloudflare tunnel in one command.

## Deploy to GitHub Pages

1. Push this repository to GitHub.
2. Go to **Settings > Pages** and set the source to **GitHub Actions**.
3. The workflow at `.github/workflows/deploy.yml` will build and deploy the site automatically on every push to `main`.

## License

This repository uses a dual license:

- **Content** (`claim_full.md`, `README.md`, and the `docs/` site pages, including the checklist elaborations) is licensed under [**CC BY-NC-ND 4.0**](LICENSE) (Attribution-NonCommercial-NoDerivatives).
- **Code** (site tooling and scripts, including `start.sh`, `docs/_config.yml`, `docs/_plugins/`, `docs/_sass/`, `docs/_includes/`, `.github/workflows/`, and `Gemfile`) is licensed under the [**MIT License**](LICENSE-CODE).

Illustrative examples and excerpts quoted from third-party published literature retain their original copyright and license terms as noted in the text and [references](docs/references.md); they are not relicensed under CC BY-NC-ND 4.0. CLAIM guideline text reproduced verbatim is included by permission of the Radiological Society of North America (RSNA) and is likewise not covered by the CC BY-NC-ND 4.0 grant.

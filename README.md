# SAMA POS Analysis — Q1 vs Q2 2026

Prepared from SAMA_Report(2).Rmd and its matching Excel input.
The workflow renders the R report as index.html and publishes it to GitHub Pages.

## Setup
1. Create a public repository named sama-pos-2026 on GitHub.
2. Upload the contents of this folder, including .github/workflows/pages.yml, to the main branch. Do not upload the ZIP itself.
3. In Settings > Pages > Build and deployment > Source, select GitHub Actions.
4. In Actions, run Build and publish SAMA report, or push a new commit.
5. The deployment URL appears in the workflow and Settings > Pages.

Expected URL after successful deployment: https://zahrah-002.github.io/sama-pos-2026/

The Rmd is rendered during the workflow; no R installation is needed on your computer.
The package has not been rendered locally because R is unavailable in this environment.
The previously generated HTML was not used because it does not match the supplied Rmd.

# Haotian Wang Homepage

This repository hosts the GitHub Pages personal academic homepage for Haotian Wang:

<https://accwht.github.io>

The site is based on the AcadHomepage Jekyll template and is configured as a user site repository: `accwht/accwht.github.io`.

## Deployment

The repository is ready to deploy as a GitHub personal homepage.

Recommended GitHub Pages setting:

1. Open `Settings -> Pages`.
2. Set `Source` to `GitHub Actions`.
3. Push to the `main` branch or manually run the `Deploy GitHub Pages` workflow.

Classic branch deployment should also work for this user-site repository if `Settings -> Pages -> Source` is set to `Deploy from a branch`, with branch `main` and folder `/ (root)`.

## Google Scholar Citations

The `Get Citation Data` workflow updates citation data for Google Scholar author ID:

```text
CbH1UJAAAAAJ
```

It runs on pushes to `main`, on a daily schedule, and manually via `workflow_dispatch`. The workflow writes generated citation JSON files to the `google-scholar-stats` branch, which powers the citation badge and per-paper citation counters.

The workflow also supports a repository secret named `GOOGLE_SCHOLAR_ID`; if the secret is absent, it falls back to `CbH1UJAAAAAJ`.

## Local Preview

Install the GitHub Pages/Jekyll environment, then run:

```bash
bash run_server.sh
```

Open <http://127.0.0.1:4000> to preview the site locally.

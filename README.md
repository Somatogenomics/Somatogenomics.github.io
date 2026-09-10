# Somatogenomics.github.io

Source for https://somatogenomics.github.io — a Quarto website listing analyses, methods, and tools by Abdulhadi (Somato) Kobiowu.

## Structure

```
_quarto.yml          site config (navbar, theme)
index.qmd            home page with featured projects
projects.qmd         auto-generated table of every file in projects/
projects/*.qmd       one page per analysis or tool
tools.qmd            software usable on its own
about.qmd
styles.scss          status badges and table styling
.github/workflows/publish.yml   renders with Quarto 1.7.32 and deploys to GitHub Pages
```

## Add a project

1. Copy any file in `projects/` and edit the YAML header: `title`, `description`, `date` (drives sort order), `categories`.
2. Put one status badge at the top: `[Public]{.status-badge .status-public}`, `[Code only]{.status-badge .status-code}`, or `[Planned]{.status-badge .status-planned}`.
3. Follow the page outline: question, data and reference versions, methods and parameters, QC and exclusions, outputs, alternative explanations / what would falsify it.
4. Commit and push to `main`; the workflow renders and deploys.

## Render locally

```
quarto preview      # live reload
quarto render       # writes _site/
```

## Repository settings required once

Settings → Pages → Source: **GitHub Actions**.

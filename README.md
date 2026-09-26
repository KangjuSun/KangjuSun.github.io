# Kangju Sun's Quarto Website

This is my personal Quarto website for DSCI 521.

It includes two computational posts:
- a Python post about my MDS study schedule
- an R post about my pool practice and weekly results

## Rebuild the website

Restore the Python environment:

```bash
uv sync
```

Restore the R environment:

```bash
R -q -e 'renv::restore()'
```

Render the website:

```bash
uv run quarto render
```

Preview the website:

```bash
uv run quarto preview
```
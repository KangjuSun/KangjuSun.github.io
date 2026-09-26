# Kangju Sun's Quarto Website

This is my personal Quarto website for DSCI 521. It includes a Python post about my MDS study plan and an R post about my pool practice.

## Software

I built the website with:

- Quarto 1.10.18
- uv 0.12.9
- R 4.6.1
- Python 3.14

Python dependencies are recorded in `pyproject.toml` and `uv.lock`.
R dependencies are recorded in `renv.lock`.

## Rebuild the Website

Clone the repository:

```bash
git clone https://github.com/KangjuSun/KangjuSun.github.io.git
cd KangjuSun.github.io
```

Restore the Python environment:

```bash
uv sync
```

Restore the R environment:

```bash
R -q -e 'renv::restore(prompt = FALSE)'
```

Render the complete website from the top level of the repository:

```bash
uv run quarto render
```

The rendered website is created in the `docs/` directory.

To preview the website locally:

```bash
uv run quarto preview
```

## Data

The Python post uses `posts/python-mds-study/study_plan.csv`. I created this small dataset from my MDS weekly schedule and rough estimates of my study time.

The R post uses `posts/r-mds-study/pool_practice.csv`. I created this small example dataset based on my pool-practice routine during the two months after finishing my undergraduate courses.

Both data files are included in this repository, so the build does not need the internet to download data. Internet access is needed when cloning the repository and when restoring packages for the first time.


# nightingale

> A minimal, well-structured **R package** for practicing and teaching research software engineering (tests, docs, CI, reproducibility).

<!-- Badges (replace links/branches as needed) -->
![R-CMD-check](https://github.com/jansim/nightingale/actions/workflows/R-CMD-check.yaml/badge.svg)
[![Codecov](https://codecov.io/gh/jansim/nightingale/branch/main/graph/badge.svg)](https://codecov.io/gh/jansim/nightingale)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Docs](https://img.shields.io/badge/docs-pkgdown-blue.svg)](https://jansim.github.io/nightingale/)

---

## Table of contents
- [Overview](#overview)
- [Quick start](#quick-start)
- [Installation](#installation)
- [Usage](#usage)
- [Project structure](#project-structure)
- [Development](#development)
- [Testing](#testing)
- [Code style & linting](#code-style--linting)
- [Reproducibility](#reproducibility)
- [Docker](#docker)
- [Contributing](#contributing)
- [Changelog](#changelog)
- [Citation](#citation)
- [License](#license)

---

## Overview
**nightingale** demonstrates a clean R package layout with tests, documentation, and automation. It’s intended as a small, practical example you can clone, extend, and use as a template.

**Highlights**
- Idiomatic R package structure (`R/`, `man/`, `tests/`, `DESCRIPTION`, `NAMESPACE`)
- Roxygen2 documentation and help pages
- Unit tests (e.g., `{testthat}`)
- Optional CI (R CMD check), coverage, and pkgdown docs
- Reproducible environments (e.g., `{renv}`) and a Dockerfile

---

## Quick start
```r
# install devtools if needed
install.packages("devtools")

# install from this branch (update branch name after merging)
devtools::install_github("jansim/nightingale@sessions/2-readme")

#Usage
library(nightingale)


```
## Development

```r
# one-time
install.packages(c("devtools", "roxygen2", "testthat", "lintr"))

# update docs & NAMESPACE
devtools::document()

# build & install
devtools::build()
devtools::install()

# full checks (recommended before PRs)
devtools::check()
```

## Testing
devtools::test()

install.packages("covr")
covr::report()

## Reproducibility
install.packages("renv")
renv::init()        # initializes project library
renv::snapshot()    # updates renv.lock after changes


## Docker
docker build -t nightingale:dev .


<!-- README.md is generated from README.Rmd. Please edit that file -->

# Overview

A data science project built with [quarto](https://quarto.org/) and
[targets](https://books.ropensci.org/targets/).

# Setup

- Create an R script called `_targets_config.R` in the project root
  directory with the following objects and populate:

<!-- -->

    # Config file for targets pipeline (not tracked by git). Defines global
    # objects that may differ between local instances of a project.

    # File paths ---------------------------------------------------------------

    # input files
    PREVIOUS_CODELISTS_DIR <-
    HDRUK_MAPPED_CSV_IN_PATH <-

- Create a `.Renviron` file in the project root directory, specifying
  the paths to your local copy of `all_lkps_maps.db` and your targets
  config file (if using a different file) e.g. 

<!-- -->

    ALL_LKPS_MAPS_DB=~/Documents/Data/all_lkps_maps_sct.db
    TARGETS_CONFIG=_targets_config_alternative.R

- Install required R packages, ideally using
  [renv](https://rstudio.github.io/renv/) with `renv::init()`, or
  `renv::restore()` if a `renv.lock` file is already present.
- Run [targets pipeline](https://books.ropensci.org/targets/) with
  `tar_make()` in the R console.

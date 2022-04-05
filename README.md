<!-- README.md is generated from README.Rmd. Please edit that file -->

# demo.compendium

<!-- badges: start -->

[![License: GPL (&gt;=
2)](https://img.shields.io/badge/License-GPL%20%28%3E%3D%202%29-blue.svg)](https://choosealicense.com/licenses/gpl-2.0/)
[![Dependencies](https://img.shields.io/badge/dependencies-3/70-green?style=flat)](#)
<!-- badges: end -->

Research Compendium of the project **{{ PLEASE ADD A FEW WORDS }}**

### How to cite

Please cite this compendium as:

> **{{ PLEASE ADD A CITATION }}**

### Content

This repository is structured as follow:

-   [`data/`](https://github.com/ahasverus/demo.compendium/tree/master/data):
    contains all raw data required to perform analyses

-   [`analyses/`](https://github.com/ahasverus/demo.compendium/tree/master/analyses/):
    contains R scripts to run each step of the workflow

-   [`outputs/`](https://github.com/ahasverus/demo.compendium/tree/master/outputs):
    contains all the results created during the workflow

-   [`figures/`](https://github.com/ahasverus/demo.compendium/tree/master/figures):
    contains all the figures created during the workflow

-   [`R/`](https://github.com/ahasverus/demo.compendium/tree/master/R):
    contains R functions developed especially for this project

-   [`man/`](https://github.com/ahasverus/demo.compendium/tree/master/man):
    contains help files of R functions

-   [`DESCRIPTION`](https://github.com/ahasverus/demo.compendium/tree/master/DESCRIPTION):
    contains project metadata (author, date, dependencies, etc.)

-   [`make.R`](https://github.com/ahasverus/demo.compendium/tree/master/make.R):
    main R script to run the entire project by calling each R script
    stored in the `analyses/` folder

### Usage

-   Clone this repository
-   Open a terminal
-   Build the Docker image with:

<!-- -->

    docker build -t "demo.compendium" .

-   Start a container based on this image:

<!-- -->

    docker run --rm -p 127.0.0.1:8787:8787 -e DISABLE_AUTH=true demo.compendium

-   On a web browser enter this URL: `127.0.0.1:8787`. A new RStudio
    Server instance will be available.
-   To run the analysis:

<!-- -->

    source("make.R")

### Notes

-   All required packages, listed in the `DESCRIPTION` file, will be
    installed (if necessary)
-   All required packages and R functions will be loaded
-   Some analyses listed in the `make.R` might take time

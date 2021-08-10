# GitHub Test Repo

This repository is for familiarizing myself with GitHub

## Goals and Objectives

## Getting Started

[Conduct](CONDUCT.md) - Code of contact for contributing to the project

[Development](DEVELOPMENT.md) - Instructions for branching and development to protect the main production code

[Contributing](CONTRIBUTING.md) - Instruction for those not on the MAPS dev team to contribute modules or code through pull requests

[R style guide](https://style.tidyverse.org/) - Info on the R style, following the tidyverse guidelines

[Issues](https://github.com/NOAA-Fisheries-Greater-Atlantic-Region/MAPS/issues) - Place to post issues and ideas


## Setup

First start by getting a configuration file set up. You can copy this in from another directory or use the convenience function to create a template to fill in with the values. You can run the following in R to set it up:

```
source("Code/R/Functions/write_config.r")

write_config()
```

Next open the resulting `config.yml` file. Type in the database information, usernames, and passwords for the desired schema and settings. Save the file. Back in R you can use the `config` package to read the results into R as objects:

```
# get the default
settings <- config::get()
settings$uid

# get a specific config set
fso <- config::get(config = "fso")
fso$pwd

# get from a config file in a different directory
config::get(config = "apsd", file = "tmp/config.yml")
```

## Use

Instructions for running, testing, and evaluating code and output. **coming soon**


## Disclaimer

*This repository is a scientific product and is not official communication of the National Oceanic and Atmospheric Administration, or the United States Department of Commerce. All NOAA GitHub project code is provided on an 'as is' basis and the user assumes responsibility for its use. Any claims against the Department of Commerce or Department of Commerce bureaus stemming from the use of this GitHub project will be governed by all applicable Federal law. Any reference to specific commercial products, processes, or services by service mark, trademark, manufacturer, or otherwise, does not constitute or imply their endorsement, recommendation or favoring by the Department of Commerce. The Department of Commerce seal and logo, or the seal and logo of a DOC bureau, shall not be used in any manner to imply endorsement of any commercial product or activity by DOC or the United States Government.*

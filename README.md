[![DOI](https://zenodo.org/badge/736473737.svg)](https://zenodo.org/doi/10.5281/zenodo.10999522)

# GPR68 sequencing and DMS QC

## Description
This repository contains data and code pertaining to ["Molecular basis of proton-sensing by G protein-coupled receptors," Matthew K Howard, Nicholas Hoppe, Xi-Ping Huang, Christian B Macdonald, Eshan Mehrotra, Patrick Rockefeller Grimes, Adam M Zahm, Donovan D Trinidad, Justin G English, Willow Coyote-Maestas, Aashish Manglik bioRxiv 2024.04.17.590000; doi: https://doi.org/10.1101/2024.04.17.590000](https://doi.org/10.1101/2024.04.17.590000).

The code in this repository is specific to the QC and analysis of the DMS data in this publication.

The pipeline used to generate these results is available in the following repository: https://github.com/odcambc/GPR68_processing

## Table of Contents
- [DMS Analysis Stub](#dms-analysis-stub)
  - [Description](#description)
  - [Table of Contents](#table-of-contents)
  - [Reproducing](#reproducing)
  - [Usage](#usage)
    - [File Structure](#file-structure)
  - [Citations](#citations)
  - [License](#license)
  - [Contributing](#contributing)

## Reproducing
Clone the repository into a new directory:
```
git clone https://github.com/odcambc/GPR68_DMS_QC.git
```

After cloning, you will need to initialize the repository. If you are using rstudio, you can do this by opening the project file `GPR68_QC.Rproj`, then initializing the environment with the comment `renv::restore()`.

Otherwise, you can initialize the repository by running the following command from the root directory of the repository:

```
Rscript -e 'renv::restore()'
```

You can then open the rstudio project file `GPR68_QC.Rproj` to view the code used to generate the figures, as well as the raw
data and MultiQC reports.

## Usage
### File Structure
The following files are contained in this repository:
```
├── analysis
│   ├── functions
│   │   ├── dms_analysis_utilities.r 
│   │   ├── map_pdb.r
│   │   ├── mkh_heatmap_function.R
│   │   ├── plot_heatmap.r
│   │   └── plot_scatter.r
│   ├── gpr68_dms_counts.Rmd
│   └── gpr68_dms_scores.Rmd
├── data
│   ├── counts
│   │   └── (Observed counts files here)
│   ├── scores
│   │   └── (Put the starting score files in here)
│   └── sequences
│       └── (GPR68 WT fasta file)
├── GPR68_QC.Rproj
├── LICENSE
├── README.md
├── renv
│   └── ...
└── results
    └── plots
        ├── heatmaps
        │   └── (Output heatmaps will be put in here)
        ├── histograms
        │   └── (Output heatmaps will be put in here)    
        └── scatterplots
            └── (Output scatterplots will be put in here)
```

## Citations
This workflow is built off of a stub analysis workflow we developed: see https://github.com/odcambc/dms_analysis_stub

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

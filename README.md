# DMS Analysis Stub

## Description
This repository contains data and code pertaining to Howard, Hoppe, et al 2023.

The code in this repository is specific to the QC and analysis of the DMS data in this publication.

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
This workflow, is built off of a stub analysis workflow we developed: see https://github.com/odcambc/dms_analysis_stub

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## Contributing
Pull requests and issues are welcome and appreciated.

# Reproducible Package for _"Smart card systematic mapping review analysis"_

[![nbviewer](https://raw.githubusercontent.com/jupyter/design/master/logos/Badges/nbviewer_badge.svg)](https://github.com/GeoTecINIT/smartcard-systematic-mapping-review/)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GeoTecINIT/smartcard-systematic-mapping-review/HEAD?labpath=Analysis.ipynb)
[![Paper DOI]()]()
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.13378710.svg)](https://doi.org/10.5281/zenodo.13378710)

The following [Jupyter Notebook](./Analysis.ipynb) is in charge of the analysis for the smart card systematic mapping review. This
systematic mapping review aims to comprehensively examine the current state-of-the-art in using 
smart cards for analytical studies applied to public transportation research. The review focuses on 
identifying and analyzing the main analytical purposes, algorithmic approaches, methods, datasets, 
and trends employed in these studies.

The methodology followed the [PRISMA statement](http://www.prisma-statement.org/) for systematic reviews. 
This code is used for obtaining the results after extracting the data from the selected studies.

## Libraries used

Python 3.11 was used for the analysis and the libraries and dependencies are defined in `requirements.txt`. 
The main libraries used are:

- [numpy](https://numpy.org/)
- [pandas](https://pandas.pydata.org/)
- [matplotlib](https://matplotlib.org/)
- [seaborn](https://seaborn.pydata.org/)
- [plotly](https://plotly.com/python/)
- [scikit-learn](https://scikit-learn.org/stable/index.html)
- [osmnx](https://osmnx.readthedocs.io/en/stable/)
- [pybtex](https://pybtex.org/)

## Initial data

Two sources of data available in the [datasets folder](./datasets/):
- Extracted data from the selected studies. `datasets/Cleaned_data.xlsx`
- Bibliometric data from online databases. `datasets/savedrecs.txt`

## Results

Some results are included in the Jupyter Notebook, like latex tables and extracted summaries, others 
like plots and diagrams are in the [images folder](./img/)

## Reproducibility

### Reproduce online
Click the on the "Binder" badge above to open an interactive Jupyter environment with all required software installed.


### Reproduce locally
Install Python 3.11, download the repository, open a command line in the root of the directory and install the required software by executing:

```bash
pip install -r requirements.txt
```

### Reproduce locally with Docker
Install [Docker](https://www.docker.com) for building an image based on a `Dockerfile` with a Jupyter environment and running a container based on the image.

Download the repository, open a command line in the root of the directory and:

1. Build the image:

```bash
docker build . --tag smat-card-systematic-mapping-review
```

2. Run the image:

```bash
docker run -it -p 8888:8888 smat-card-systematic-mapping-review
```

3. Click on the login link (or copy and paste in the browser) shown in the console to access to a Jupyter environment.

### Reproduce the analysis
Open the Jupyter Notebook (Analysis.ipynb) file. The notebook contains the used code and its outputs. You can execute
the code to reproduce the obtained results.

> [!NOTE] 
> When executing an analysis with a component of randomness (i.e., ML models training), the obtained results could be slightly different
than the reported ones. Notwithstanding, the conclusions should be similar as the reported ones.

> [!WARNING] 
> `osmnx` library is used for searching the locations of the locations of the institutions of the authors' affiliations. It generates a local cache of the locations, it seems that deleting the cache after some time might require editing the specific cell, because Open Street Map might introduce changes and make it difficult to locate some institutions.
PLEASE REVISE THIS CELL AND MANUALLY MODIFY IF NECESSARY
# Smart card systematic mapping review analysis

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

## Initial data

Two sources of data available in the [datasets folder](./datasets/):
- Extracted data from the selected studies. `datasets/Cleaned_data.xlsx`
- Bibliometric data from online databases. `datasets/savedrecs.txt`

## Results

Some results are included in the Jupyter Notebook, like latex tables and extracted summaries, others 
like plots and diagrams are in the [images folder](./img/)

## How to run the code

Jupyter Notebook is needed to open the [provided code](./Analysis.ipynb).

The python libraries dependencies are provided in the `requirements.txt` file and should be 
installed using the command `python pip install -r requiorements.txt`.

The execution time is around 1 minute but could be slower the first time because some libraries 
need to download some files.
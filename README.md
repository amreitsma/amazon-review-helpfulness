# Helpfulness votes on Amazon: what makes online reviews helpful?
This repository includes all the code needed to carry out my research on amazon review helpfulness in the form of a Jupyter Notebook, and a txt file providing the necessary requirements to run it.

## Getting Started

These instructions will get you a copy of the project up and running on your local Linux machine. 

### Prerequisites

To open this project, the necessary requirements must be installed. Download the files and install all the packages:

```
$ cd research_project
$ pip3 install -r requirements.txt
```

### To open the notebook

Once everything is installed, start Jupyter Notebooks as follows:

```
$ jupyter notebook
```
This should open the Jupyter interface in your browser. Navigate to the directory containing the code and open the .ipynb file to see the code. To properly initialize the notebook, make sure to clik "cell" and then "run all".

### Data
Datasets for this notebook can be downloaded [here](https://nijianmo.github.io/amazon/index.html)

The dataset I used in my research was the 5-core dataset for category Industrial and Scientific. Another 5-core dataset would work as well, but then you would have to change the filename in the code itself and the mean review length. Make sure not to use any datasets larger than the Industrial and Scientific datasets, otherwise Jupyter may crash.

To use another dataset, change the filename in the following code to the filename of the dataset you're using
```
df = getDF("Industrial_and_Scientific_5.json.gz")
```
and then change "53" (mean review length) to the mean review length for your dataset.
```
df['length'] = np.where(df['reviewLength']>=53, 'long', 'short')
```

## Authors

* **Aïsje Reitsma** - *Initial work* - [amreitsma](https://github.com/amreitsma)

# Covid Prediction in Germany
## Covid Prediction for Germany in December 2021

Machine Learning/Deep Learning Prediction for Covid Cases

In this project, different Models including a supervised learning Neural Networks and an ensamble methood approach will be developed to predict Covid Cases for the December 2021.

**Jonathan, Satish and Kevin**

## Project Description / Problem to be solved
The main problem to be solved is to ...

### Goal
The main goal of this project is to develop a Deep Learning Regression model. This Model should be used to predict with the highest accuracy the future covid cases, for that we take into account different factor such as the Vaccination Doses.

## Data Description

tbd.
The data consists of ---  in ---:

which we will first download.
These files ... (Details here). After preprocessing we will store ....

## Model Description
tbd.
For the model we will try three different models. A simple linear model, an ensemble model and lastly a multi-layer dense neural network. This is not the state-of-the-art solution for this taks, but serves as a simple first idea benchmark.

## Results Overview
tbd.
Results here. For example:
Prediction accuracy per model:

* Pandemic Model - 90%
* Ensemble - 85%
* Recurrent Neural Network - 80%

Examples of correct predictions:

Misclassification confusion matrix:

Examples of wrong predictions:


## Project structure

The Goal here is that you write one or two sentences explaining what is in the folders of your structure and how the structure looks like

```
.
├── conf               <- Space for credentials (included in )
│
├── data
│   ├── 01_raw         <- Immutable input data (included in )
│   ├── 02_intermediate<- Cleaned version of raw
│   ├── 03_processed   <- Data used to develop models
│   ├── 04_models      <- trained models
│   ├── 05_model_output<- Model output
│   └── 06_reporting   <- Reports and input to PPTX,frontend,GUI,...
│
│
├── notebooks          <- Jupyter notebooks. Naming convention is
|                         date YYYYMMDD (for ordering),
│                         the nt-user, and a short `_`
|                         delimited description. (e.g.
|                         20200313_ril3si_template.ipynb)
│
├── references         <- Data dictionaries, manuals, etc.
│
├── results            <- Final analysis documentation.
│
│
├── src                <- Source code for use in this project (mirroring
│   │                     the data/ folder).
│   ├── __init__.py    <- Makes src a Python module
│   │
│   ├── __main__.py    <- The main procedure of the project
│   │
│   ├── d00_utils      <- Functions used across the project
│   │   └── e.g. remove_accents.py
│   │
│   ├── d01_data       <- Scripts to reading and writing data etc
│   │   └── load_data.py
│   │
│   ├── d02_intermediate<- Scripts to transform data from raw to
│   |   |                  intermediate
│   │   └── create_int_data.py
│   │
│   ├── d03_processing <- Scripts to turn intermediate data into
│   |   |                 modelling input
│   │   └── create_input_data.py
│   │
│   ├── d04_modelling  <- Scripts to train models and then use
│   |   |                  trained models to make predictions.
│   │   └── train_model.py
│   │
│   ├── d05_model_evaluation<- Scripts that analyse model
│   |   |                      performance and model selection.
│   │   └── calculate_performance_metrics.py
│   │
│   └── d06_reporting_and_visualization  <- Scripts to produce reporting
│       |                                   tables
│       └── e.g. create_reporting_summary.py
│
├── .gitignore         <- Avoids uploading data, credentials,
|                         outputs, system files etc
│
├── LICENCE            <- The project licence.
│
├── mnist.py           <- The script to run the project.
│
├── README.md          <- The top-level README for developers.
│
└── requirements.txt   <- The requirements file for reproducing the
                          analysis environment via pip.
```
## Example Coding Workflow

1) Start by prototyping in a jupyter notebook (e.g. get to know your data, data cleansing, ...)
2) Refactor a working code snippet as a function within the notebook.
3) Test the function.
4) Move the function into the src folder as a python file (to increase modularity and reusability).
5) Import & Test the function in the jupyter notebook.
6) Write a main project script.

How to import functions into a notebook:  
First we tell the notebook where the functions are

```python
import os
import sys
src_dir = os.path.join(os.getcwd(), '..', 'src')
sys.path.append(src_dir)
```

Then we state which functions to import

```python
from d00_utils.functionname import functionname
```

See how nicely this ties into the standardized project structure?

### How use a template environment

To guarantee reproducability of results, it is a best-practise to export your project coding environment for others. The following commands show you how to do it.

#### Save environment

``pip freeze > requirements.txt``

#### Load environment

``conda create -n example_project python=3.6 -y``  
``conda activate example_project``  
``pip install -r requirements.txt``  

---
Read more at: [Pipelines and Project Workflow](https://github.com/dssg/hitchhikers-guide/tree/master/sources/curriculum/0_before_you_start/pipelines-and-project-workflow)

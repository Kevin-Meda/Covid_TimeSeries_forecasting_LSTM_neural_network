# Covid_Prediction_Germany
Covid Prediction for Germany in December 2021

Machine Learning Prediction for Covid Cases

In this project, an suoervised learning Neural Networks approach will be developed to predict Covid Cases for the December 2021.

Project Description / Problem to be solved
The main problem to be solved is to find a phenomena within the data without having a reference dataset. This means no supervised learning method is applicable. To solve this, we are applying unsupervised learning methods, to find anomalies within the data. After finding these anomalies, the corresponding data needs to be inspected and analyzed by domain experts to provide some explanation. Thus, the algorithm will be refined and the data better understood and validated. Following this strategy will lead to new findings, e.g. early detection of unknown failure modes and / or the finding of the black deposit phenomena.

Goal
The main goal of this project is to develop a Deep Learning Regression model. This Model should be used to predict with the highest accuracy the future covid cases, for that we take into account different factor such as the Vaccination Doses.

Data Description
tbd.
The data consists of ---  in ---:

Test Images : t10k-images-idx3-ubyte
Test Labels : t10k-labels-idx1-ubyte
Train Images : train-images-idx3-ubyte
Train Labels : train-labels-idx1-ubyte

which we will first download.
These files use the IDX file format (Details here). After preprocessing we will store these images as four numpy arrays consisting of two arrays for the images (28x28 px greyscale values between 0-255) and two arrays for the correct image lables (the number which is written in the image) between 0-9.

Model Description
tbd.
For the model we will try three different models. A simple linear model, an ensemble model and lastly a multi-layer dense neural network. This is not the state-of-the-art solution for this taks, but serves as a simple first idea benchmark.

Results Overview
tbd.
Results here. For example:
Prediction accuracy per model:

Pandemic Model - 90%
Ensemble - 85%
Recurrent Neural Network - 80%

Examples of correct predictions:

Misclassification confusion matrix:

Examples of wrong predictions:


Project structure
The structure of the project doesnt need to be complicated. I have copied a structure below as a template. You dont need to follow it.
The Goal here is that you write one or two sentences explaining what is in the folders of your structure and how the structure looks like :-)
.
├── conf               <- Space for credentials (included in .gitignore)
│
├── data
│   ├── 01_raw         <- Immutable input data (included in .gitignore)
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


How use a template environment
To guarantee reproducability of results, it is a best-practise to export your project coding environment for others. The following commands show you how to do it.

Save environment
pip freeze > requirements.txt

Load environment
conda create -n example_project python=3.6 -y
conda activate example_project
pip install -r requirements.txt

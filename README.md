# Covid Deaths Prediction in Germany
## LSTM RNN for Multivariate Timeseries

__Machine Learning/Deep Learning Prediction for Covid Deaths__

In this project, a LSTM Recurrent Neural Networks based on TensorFlow is developed to predict the Covid Deaths in Germany for the following  based on cases, recovered people and vaccinated people

#### Data Source (3 datasets): https://www.kaggle.com/headsortails/covid19-tracking-germany
### __Tableau Dashboard__ created to interact with datasets: 
#### https://public.tableau.com/views/CovidDeathsinGermanybyStateandAgeGroup/CovidAnalysisinGermany?:language=en-US&:display_count=n&:origin=viz_share_link
![alt text](https://github.com/Kevin-Meda/Covid_TimeSeries_Prediction_Germany/blob/main/Covid%20Analysis%20in%20Germany.png)

### Final Predictions
![alt text](https://github.com/Kevin-Meda/Covid_TimeSeries_Prediction_Germany/blob/main/Deaths_Prediction.JPG)

**Jonathan, Satish and Kevin**

## Project Description / Problem to be solved
The main problem to be solved is to predict the amount of deaths in the following 2 weeks depending on the amount of cases, receovered people and vaccination with 1 and 2 doses.

### Goal
The main goal of this project is to develop a Deep Learning Recurrent Neural Network Long Short Term Memory (RNN LSTM) model. This Model should be used to predict with the highest accuracy the future covid deaths, for that we take into account different factor such as the Vaccination Doses.

## Data Description tbd
tbd.
The data consists of ---  in ---:

which we will first download.
These files ... (Details here). After preprocessing we will store ....

## Model Description 
For the model we will try two different LSTM RNN models. The first one is with the the Tensor Flow Keras Libray and the second is with Pytorch. These are some of state-of-the-art solution for this taks and serve as a good benchmark for new models.

### Recurrent Neural Network (RNN)
Recurrent Neural Network is a generalization of feedforward neural network that has an internal memory. RNN is recurrent in nature as it performs the same function for every input of data while the output of the current input depends on the past one computation. After producing the output, it is copied and sent back into the recurrent network. For making a decision, it considers the current input and the output that it has learned from the previous input.
Unlike feedforward neural networks, RNNs can use their internal state (memory) to process sequences of inputs. This makes them applicable to tasks such as unsegmented, connected handwriting recognition or speech recognition. In other neural networks, all the inputs are independent of each other. But in RNN, all the inputs are related to each other.

### Long Short Term Memory (LSTM)
Long Short-Term Memory (LSTM) networks are a modified version of recurrent neural networks, which makes it easier to remember past data in memory. The vanishing gradient problem of RNN is resolved here. LSTM is well-suited to classify, process and predict time series given time lags of unknown duration. It trains the model by using back-propagation. 
In an LSTM network, three gates are present:
*Input gate — discover which value from input should be used to modify the memory. Sigmoid function decides which values to let through 0,1. and tanh function gives weightage to the values which are passed deciding their level of importance ranging from-1 to 1.
*Forget gate — discover what details to be discarded from the block. It is decided by the sigmoid function. it looks at the previous state(ht-1) and the content input(Xt) and outputs a number between 0(omit this)and 1(keep this)for each number in the cell state Ct−1.
*Output gate — the input and the memory of the block is used to decide the output. Sigmoid function decides which values to let through 0,1. and tanh function gives weightage to the values which are passed deciding their level of importance ranging from-1 to 1 and multiplied with output of Sigmoid.
Long Short Term Memory (LSTM)![alt text](https://user-images.githubusercontent.com/67469727/150086251-d4148b14-f25a-4b2b-b66c-81a12e9ba39c.png)

Data Source:
https://aditi-mittal.medium.com/understanding-rnn-and-lstm-f7cdf6dfc14e

## Results Overview tbd
tbd.
Results here. For example:
Prediction accuracy per model:

* Pandemic Model - 90%
* Ensemble - 85%
* Recurrent Neural Network - 80%

Examples of correct predictions:

Misclassification confusion matrix:

Examples of wrong predictions:


## Project structure tbd
tbd.
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

To guarantee reproducability of results, it is a best-practise to export your project coding environment for others.   

---
Read more at: [Pipelines and Project Workflow](https://github.com/dssg/hitchhikers-guide/tree/master/sources/curriculum/0_before_you_start/pipelines-and-project-workflow)

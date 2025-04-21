# California Housing Price Prediction

We are trying to predict housing prices in california. The dataset is from [Kaggle](https://www.kaggle.com/datasets/camnugent/california-housing-prices).
The chosen Data science lifecycle is CRISP-DM.


## 📖 Table of Contents
1. [Prerequisites](#prerequisites)  
2. [⚙️ Setup Guide](#️setup-guide)  
   - [Create a Virtual Environment](#1️⃣-create-a-virtual-environment)  
   - [Install Dependencies](#2️⃣-install-dependencies)  
   - [Run the Project](#run-the-project)  
3. [Project Organization](#project-organization)  
4. [Results](#results)  
5. [For Contributors: Configuring Git for Jupyter Notebooks](#for-contributors-configuring-git-for-jupyter-notebooks)  

## Prerequisites

Project works on:
- Python 3.13.2
- pip 25.01


## ⚙️ Setup Guide

After you have cloned the repo and are in the root of the project run the following commands:

### 1️⃣ Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
```

### 2️⃣ Install Dependencies
```
pip install -r requirements.txt
```

### Run the project

- The whole documentation and code can be found in `notebooks/california_houseprices_crispdm.ipynb`. 


## Project Organization

For the project structure we used [Cookie-Cutter](https://cookiecutter-data-science.drivendata.org/). 
Since this is a simple ML-project and not a whole automated ML-System with pipelines, we  just make use of the notebooks folder where you can find the code and the data folder, where our data is stored.

```
├── Makefile           <- Makefile with convenience commands like `make data` or `make train`
├── README.md          <- The top-level README for developers using this project.
├── data
│   ├── external       <- Data from third party sources.
│   ├── interim        <- Intermediate data that has been transformed.
│   ├── processed      <- The final, canonical data sets for modeling.
│   └── raw            <- The original, immutable data dump.
│
├── docs               <- NOT USED
│
├── models             <- Trained and serialized models, model predictions, or model summaries
│
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
│                         the creator's initials, and a short `-` delimited description, e.g.
│                         `1.0-jqp-initial-data-exploration`.
│
├── pyproject.toml     <- Project configuration file with package metadata for 
│                         california_housing_price_prediction and configuration for tools like black
│
├── references         <- NOT USED
│
├── reports            <- NOT USED
│   └── figures        <- NOT USED
│
├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
│                         generated with `pip freeze > requirements.txt`
│
├── setup.cfg          <- Configuration file for flake8
│
└── california_housing_price_prediction   <- Source code for use in this project.
    │
    ├── __init__.py             <- Makes california_housing_price_prediction a Python module
    │
    ├── config.py               <- NOT USED
    │
    ├── dataset.py              <- NOT USED
    │
    ├── features.py             <- NOT USED
    │
    ├── modeling                
    │   ├── __init__.py 
    │   ├── predict.py          <- NOT USED
    │   └── train.py            <- NOT USED
    │
    └── plots.py                <- NOT USED
```

--------

## Results

**Results of our best Model:**

|      Model      |    R²    |      RMSE       |       MAE        |
|---------------|----------|----------------|----------------|
| XGBoost      | 0.839152 | 45910.471093   | 30029.313347   |

## For Contributors: Configuring Git for Jupyter Notebooks
Enable Automatic Output Stripping for Notebooks to prevent unnecessary notebook output changes in Git commits:
```
pre-commit install
```

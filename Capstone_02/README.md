Capstone_02
==============================

Analyze COVID-19 data against health and population indicators.

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

Data definition:
Country: Country where COVID-19 cases were tested
Comfirmed/Deaths/Recovered/Active: total number of different stages of COVID-19 cases
(Date of COVID-19 test is given in filename)
Cardio(vascular) death rate: percentage population that died of cardiovascular disease in 2017
Diabetes Percentage: percentage of population infected with diabetes
Obesity/Undernourished: percentage of population suffering from obesity/undernourishment (in 2018)
PopFemale/PopMale/PopTotal: Male/Female/Total Percentage of total population over the age of 75 (inclusive) in 2019
Total Population: total population in 2019

Sources:
COVID-19: https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_daily_reports/######.csv (insert date)
Cardiovascular disease: https://ourworldindata.org/grapher/cardiovascular-death-rate-vs-gdp-per-capita
Diabetes: https://ourworldindata.org/grapher/diabetes-prevalence
Obesity and Undernourished: https://www.kaggle.com/mariaren/covid19-healthy-diet-dataset
Age and population: https://population.un.org/wpp/Download/Standard/CSV/

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>

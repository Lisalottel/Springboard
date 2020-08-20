Capstone_02
==============================

Analyze COVID-19 data against health and population indicators.

Project Organization
------------

    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── final.         <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is "COVID-19_" + a number (for ordering), 
    │                         and a short "-" delimited description, e.g. "COVID-19_02-DataWrangling".
    │
    ├── references         <- Additional explanatory materials and context.
    │
    ├── reports            <- PDF and LaTeX of report, presentation
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
--------

## Data definition:
- Country: Country where COVID-19 cases were tested
- Comfirmed/Deaths/Recovered/Active: total number of different stages of COVID-19 cases (Date of COVID-19 test is given in filename)
- Cardio(vascular) death rate: percentage population that died of cardiovascular disease in 2017
- Diabetes Percentage: percentage of population infected with diabetes in 2017
- Obesity/Undernourished: percentage of population suffering from obesity/undernourishment (in 2018)
- PopFemale/PopMale/PopTotal: Male/Female/Total Percentage of total population over the age of 75 (inclusive) in 2019
- Total Population: total population in 2019

## Sources:
- COVID-19: https://raw.githubusercontent.com/CSSEGISandData/COVID-19/master/csse_covid_19_data/csse_covid_19_daily_reports/######.csv (insert date)
- Cardiovascular disease: https://ourworldindata.org/grapher/cardiovascular-death-rate-vs-gdp-per-capita
- Diabetes: https://ourworldindata.org/grapher/diabetes-prevalence
- Obesity and Undernourished: https://www.kaggle.com/mariaren/covid19-healthy-diet-dataset
- Age and population: https://population.un.org/wpp/Download/Standard/CSV/

## Notebooks
### COVID-19_01-DataWrangling
Raw data is read in, cleaned and merged into three data sets: COVID_base.csv, COVID_base_GDP.csv and Demographics_base.csv . The first is used for the further analysis, the second only for the introductury scatter plot (Scatter_Pop_Con_GDP_labeled.png) and the third did not find usage in this project. It contains health statistics and demographics for all nations that are not affected by COVID-19 on the day of the analysis.

The cleaning process mainly involved rescaling to the same units and identifying different labeling for the same countries.

### COVID-19_02-EDA
The exploratory analysis involved scatter plots, boxplots, heatmaps and pairplots to identify covariance within the data set and outliers. Additionally, clusters were defined and added as additional information to the data set.

### COVID-19_03-Preprocessing_Training
Based on the EDA findings, covariant features are dropped. For the clusters, dummy features are created. Then the data is standardized to avoid biases due to the different scales of the data. Additionally, a data set with the mortality of COVID-19 is created which was intended for a separate modeling study that does not use ANY COVID-19 as input. First modeling results were not very promising and the study has been abandonned. Finally, the data was split in a testing (25%) and a training (75%) data set, respecitvely.

### COVID-19_04-Modeling_Deaths
The fatality of COVID-19 is modeled with 4 different regression models: Polynomial Regression, Decision Tree, Random Forest and Gradient Boosting. The best performing model is the Polynomial Regression model. The most important features for all models are the number of confirmed cases, the size of the male population above age 75, and the diabetes rates.


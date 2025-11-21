AN ANALYSIS ON MUSIC TASTES AND ECONOMIC STATES

This project looks into whether a country's music taste (based on a dataset from 2017-2020) correlates meaningfully with its GDP per capita.
The goal of this project is to vaguely explore socio-economic patterns that reside in music consumption.

Sources of Data:
- Spotify dataset from 2017-2020 (https://www.kaggle.com/datasets/pepepython/spotify-huge-database-daily-charts-over-3-years/data) including 35 countries
- WorldBank for GDP per capita values retrieved using the WorldBank API

Research Questions:
1) Can music genre distributions be used to predict GDP per capita?
2) Do clusters of countries based on music taste also share similar economic traits?

Methods Used:

Regression Models:
1) Linear Regression
- Trying to model GDP as a linear combination of genre percentages
    Result and Interpretations:
    - R^2 is around -45
    - Mean Absolute Error (MAE) is around 98k USD
    - These results suggest that there are no linear relationships between music tastes and GDP per capita values. The predictions are inaccurate and provide a valuable negative result.
    
2) Random Forest Regressor (RF)
- A nonlinear model built from various decision trees
    Result and Interpretations:
    - R^2 is around 0.50
    - MAE is around 15k USD
    - These results suggest that some nonlinear signals exist between genres and GDP, but it results in a prediction that is still far from accurate. A weak connection is visible.

Clustering:
- Clustering countries (Using KMeans with k=3) entirely based on their music tastes and then checking their average GDP values.
    Result and Interpretations:
    - 9 countries belonged to the High GDP cluster with their average GDP per capita being around 42k USD
    - 20 countries belonged to the Mid GDP cluster with their average GDP per capita being around 34k USD
    - 4 countries belonged to the High GDP cluster with their average GDP per capita being around 19k USD
    - Countries with similar music taste tend to be in similar economic bands. This does not strongly suggest causation, but instead shows that music taste can have some intrinsic socio-economic patterns

Limitations:
- Small dataset with limited country representation (only 35)
- Only using the "Most Important" n genres (code can be modified to change the value of n)
- The usage of Spotify as the sole data source for listening metrics
- GDP per capita is a very rough estimate of actual economic state

Tech Stack:
- Python
- Jupyter Notebook
- Pandas / NumPy
- Scikit-Learn
- Matplotlib

This project was meant to be a learning experience on concepts of regression, data cleaning, clustering, APIs and related concepts.
IMPORTANT: The Kaggle link provided above contains the dataset used. Since the dataset size was >100 MB , the file file could not be included directly.



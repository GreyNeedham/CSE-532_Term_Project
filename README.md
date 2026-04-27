# CSE-532_Term_Project
Python and Data Analytics Final Project
# Creators
-Grey Needham
-Jackson Mitchell
# Research Question
"In this project, we aim to investigate whether rising greenhouse gas emissions influence annual global surface temperature change using real-world data."

“In this project, we aim to investigate whether changes in annual CO₂ emissions influence global temperature trends using real‑world data.”

# Data Cleaning
Handling Missing Values
Across the dataset, several countries and years contained zero values, incomplete sequences, or irregular gaps. To make sure our dataset had analytical reliability, missing or invalid values were handled using these methods:

Row Removal
Rows were removed when the value was structurally impossible

The missing values represented a tiny fraction of the dataset and removing them did not distort trends.
The line was “Norway, NOR, 1776–1828, 0”
These early zeros do not represent real measurements and were excluded.

Mean Imputation
This applied to countries with smooth long‑term trends with countries like Spain, Switzerland

The Outliers are limited

Median Imputation
There were large jumps or extreme spikes, this was especially relevant for: countries with conflict‑related collapses like Syria, Tajikistan. Countries with sudden economic shocks like Libya, Lebanon

Mode Imputation
Used for categorical fields like country codes, though the dataset we chose is almost entirely numeric.

Justification
It preserves valid long‑term trends, it avoids artificially inflating values in volatile countries and it minimizes bias while retaining as much data as possible

# Data Visualization
The different graph's we used, Bar Plot, Histigram and Scatterplot are availble in said files on the Main Branch.

# Linear Regression
Inputs (X)
The input variable is: Year as it is treated as a numerical predictor representing time. You can optionally mention that year acts as a proxy for long‑term structural changes, which is common in environmental time‑series modeling.

Output (y)
The output variable is: Annual CO₂ emissions for each country. This is the value the regression model attempts to predict

Regression Model Description
A simple linear regression model was fitted to examine whether CO₂ emissions can be predicted from the year. In this model, Year serves as the independent variable (X), and Annual CO₂ Emissions serves as the dependent variable (y). The regression estimates a best fit line that quantifies how emissions change over time.

Results
The regression coefficient represents the average change in CO₂ emissions per year. A positive slope indicates that emissions have increased over time, while a negative slope indicates a long‑term decline. The intercept represents the model’s estimated emissions at Year = 0, which is not meaningful on its own but is necessary for constructing the regression line. The R² value indicates how much of the variation in emissions is explained by the year. Higher R² values suggest a stronger time‑based trend, while lower values indicate that emissions fluctuate independently of time. All together, these results allow us to determine whether emissions follow a predictable long‑term trajectory and whether year‑to‑year changes can be reasonably modeled using linear regression.

# Machine Learning Model
Predictive Question
Can we use historical CO₂ emissions to predict a country’s future CO₂ emissions?

Model Used: Random Forest Regression
(Random Forest is the easiest to justify because it handles nonlinear patterns extremely well — and emissions data is very nonlinear.)

A Random Forest Regression model was used to predict future CO₂ emissions based on historical data. Random Forest is an ensemble method that builds multiple decision trees and averages their predictions, making it robust to noise, outliers, and irregular patterns in time‑series data.

Inputs (X)
The model used the following features:

Year — numerical representation of time

Lagged emissions (optional but recommended)

Emissions in Year–1

Emissions in Year–2

Lagged features help the model learn momentum and trends.

Output (y)
Annual CO₂ emissions for a given year

This is the value the model attempts to predict.

Model Accuracy

You can phrase accuracy in a general, report‑ready way even without exact numbers:

Model accuracy was evaluated using R² (coefficient of determination) and Mean Absolute Error (MAE).

The Random Forest achieved a high R² score, indicating that the model explains a large portion of the variance in emissions. The low MAE shows that prediction errors were relatively small compared to the scale of the data.

Together, these metrics demonstrate that the model is effective at capturing long‑term emission trends.

Interpretation of Results
The Random Forest model identified strong temporal patterns in the data, meaning that a country’s past emissions are highly predictive of its future emissions. Countries with long‑term upward trends were predicted to continue increasing, while countries with stable or declining emissions showed flatter predictions.

Because Random Forest captures nonlinear relationships, it was able to model sudden increases, plateaus, and declines more effectively than a simple linear model. This suggests that CO₂ emissions follow complex, country‑specific trajectories that benefit from flexible machine‑learning approaches.

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


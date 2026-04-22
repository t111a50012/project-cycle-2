# Project Cycle 2: Confidence Intervals and One-Sample Inference

This project utilizes the 2007 Youth Risk Behavior Survey (YRBS) dataset to perform single-sample statistical inference on adolescent behavioral choices (smoking habits) and physiological indicators (BMI percentiles).

**Team Name:** [第7組]
**Team Members:** [黃睿恩 黃柏維 楊書雅]

## Project Overview
The research focuses on two core variables:

1. **Behavioral Variable (EverCigaretteUse): Analyzing whether the proportion of adolescents who have ever tried smoking significantly deviates from the benchmark $p_0 = 0.50$.**
2. **Continuous Variable (BMIPCT): Analyzing the mean BMI percentile and evaluating its distribution characteristics.**
The analysis workflow includes data cleaning, Exploratory Data Analysis (EDA), and final statistical inference (Construction of Confidence Intervals and Hypothesis Testing).

## Project Structure
The project is organized into three main stages, corresponding to three Jupyter Notebooks:

1. **Data Check & Preprocessing (01_data_check.ipynb)**
   * **Variable Definition**: Establishing a data dictionary and recoding rules.
   * **Data Cleaning**: Handling missing values using Listwise Deletion to ensure analysis integrity.
   * **Outputs**: Generation of variable_definitions.md and recoding_rules.md for future research reference.
   
2. **Exploratory Data Analysis (02_eda.ipynb)**
   * **Visualization**
        * **Count plots to observe the frequency of smoking behavior.**
        * **Histograms and Boxplots to detect distribution shapes and outliers in BMIPCT.**
   * **Normality Check**: Q-Q plots revealed a distinct S-curve pattern, indicating a significant deviation from a normal distribution.

3. **Statistical Inference (03_inference.ipynb)**
   * **Interval Estimation: Calculating Standard Errors and constructing 95% Confidence Intervals.**
   * **Hypothesis Testing :**
        * **Z-test for Proportions**: Evaluating the smoking experimentation rate.
        * **T-test for Means**: Assessing BMI indicators.
   * **Conclusion: Quantifying the relationship between observed sample data and population benchmarks.**

## Core Findings & Recommendations
The project is organized into three main stages, corresponding to three Jupyter Notebooks:

1. **Smoking Behavior Challenge**: The study found that the proportion of smoking experimentation is significantly high (over half), suggesting that trying cigarettes has become a social norm among this demographic, requiring comprehensive public health intervention.

2. **Physiological Trends**: While the mean BMI remains relatively stable, the Q-Q plot indicates a polarized distribution.

3. **Strategic Recommendations:**
   * **Universal Intervention**: Shift the focus from individual targeting to changing social norms across the entire adolescent population.
   * **Precision Support**: Move beyond "average BMI" monitoring toward "distribution-focused" support for high-risk clusters identified in the distribution tails.

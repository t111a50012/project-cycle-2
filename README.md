# Project Cycle 2: Confidence Intervals and One-Sample Inference

This project utilizes the 2007 Youth Risk Behavior Survey (YRBS) dataset to perform single-sample statistical inference on adolescent behavioral choices (smoking habits) and physiological indicators (BMI percentiles).

**Team Name:** [第7組]
**Team Members:** [113370229黃睿恩, 111370234黃柏維, 111A50012楊書雅]

## Project Overview
The research focuses on two core variables:

## 1. Proportion Analysis: `EverCigaretteUse`
This analysis focuses on the behavioral aspect of smoking experimentation among U.S. adolescents.

* **Target:** Population proportion of U.S. adolescents who have ever tried smoking.
* **Research Question:** Does the proportion of smoking experimentation significantly differ from 0.50?
* **Benchmarks & Coding:**

| Parameter | Value | Description |
| :--- | :--- | :--- |
| **Benchmark ($p_0$)** | 0.50 | Neutral population proportion |
| **Success** | `1` | Respondent has ever tried smoking (Yes) |
| **Failure** | `0` | Respondent has never tried smoking (No) |

> **Data Cleaning:** Applied **Listwise Deletion**. Records with missing values in the smoking behavior field are excluded from the final analysis.

---

## 2. Mean Analysis: `BMIPCT` (BMI Percentile)
This analysis evaluates the distribution of BMI percentiles compared to historical standards.

* **Target:** Mean BMI percentile of U.S. adolescents.
* **Research Question:** Is the mean BMI percentile significantly different from the historical benchmark of 65.0?
* **Measurement Details:**

| Parameter | Value | Description |
| :--- | :--- | :--- |
| **Benchmark ($\mu_0$)** | 65.0 | Historical average standard |
| **Value Range** | 0.0 – 100.0 | Continuous percentile scale |

## Project Structure
The project is organized into three main stages, corresponding to three Jupyter Notebooks:

1. **Data Check & Preprocessing (01_data_check.ipynb)**
   * **Variable Definition**: Establishing a data dictionary and recoding rules.
   * **Data Cleaning**: Handling missing values using Listwise Deletion to ensure analysis integrity.
   * **Outputs**: Generation of variable_definitions.md and recoding_rules.md for future research reference.
   
2. **Exploratory Data Analysis (02_eda.ipynb)**
   * **Visual Analysis of Cigarette Use**
      * **Composition Analysis (Figure 1)**: The bar chart and pie chart reveal that 52.9% of the students have tried smoking, while 47.1% have not. This confirms that the majority of the sampled adolescent population in 2007 had experimented with cigarettes.
      * **Bootstrap Stability (Figure 2)**: The resampling distribution is centered at approximately 0.529, clearly positioned to the **right** of the red benchmark line ($p=0.50$).
      * **Statistical Implication**: Since the entire distribution (including the tails) lies above 0.50, we have strong visual evidence that the true population proportion is significantly higher than 50%. This suggests that experimentation with smoking was more common than not among the youth surveyed.

   * **Descriptive Statistics & Data Audit**
      * **Observations:**
         * **Sample Integrity**: The final analysis is based on **12,683** valid records after excluding **979** missing values.
         * **Central Tendency**: The **Mean (64.84)** is lower than the **Median (70.15)**, which is a classic indicator of a **left-skewed** distribution.
         * **Range**: The data covers the full theoretical range of percentiles from approximately **0 to 100**, with a Standard Deviation of **27.48**.
         * **Quartile Distribution**: The gap between Q1 (45.17) and Q2 (70.15) is larger than the gap between Q2 and Q3 (89.43), indicating that data points are more spread out in the lower half and more densely packed in the upper half.
         
   * **Visual Analysis: Histogram, Boxplot, and Q-Q Plot**
      * **(1) Interpretation: Histogram (Shape & Skewness)**
         * **Visual Observation**: The histogram shows a significant **left-skewed (negative skew)** distribution. The frequency of data points increases as the BMI percentile approaches 100.
         * **Data Insight**: There is a massive spike in the high-percentile range (90-100), suggesting a high concentration of students in the upper BMI categories within this specific dataset.
      * **(2) Interpretation: Boxplot (Quartiles & Outliers)**
         * **Quartile Positioning**: The median line (horizontal line inside the box) is positioned towards the upper part of the range (around 70). The box itself is stretched downwards, confirming the left-skewed nature.
         * **Outlier Diagnostic**: There are no individual circles beyond the whiskers (0 and 100), indicating that even though the distribution is skewed, all data points fall within the valid percentile range without extreme statistical outliers.
      * **(3) Interpretation: Normal Q-Q Plot (Normality Check)**
         * **Deviation from Normality**: The data points (blue dots) deviate significantly from the red reference line, especially at the lower and upper theoretical quantiles.
         * **S-Curve Pattern**: The distinct "S" shape in the Q-Q plot is a classic indicator of a non-normal distribution. Given the large sample size, we must acknowledge that while a T-test might be robust, the underlying data is strongly non-normal, which is a critical finding for our report.

3. **Strategic Recommendations (03_inference.ipynb)**
   * **Universal Smoking Intervention:** Shift from targeting individuals to changing social norms across the entire adolescent population.
   * **Beyond Averages:** Move past "average BMI" monitoring toward "distribution-focused" support for high-risk clusters identified in the upper tail.
   * **Integrated Screening:** Emphasize the interaction between lifestyle behaviors and biological outcomes in future health surveys.

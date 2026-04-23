# Recoding Rules and Benchmarks (重編碼規則與基準值)

This file documents the transformations applied to the raw data for statistical inference.

### 1. Behavioral Variable: Cigarette Use
* **Transformation**: Binary recoding.
* **Logic**: 
    * Raw value `1` (Yes) -> `1` (Success)
    * Raw value `2` (No) -> `0` (Failure)
* **Neutral Benchmark ($p_0$)**: 0.50 (To test if more than half of the population experimented with smoking).

### 2. Continuous Variable: BMI Percentile
* **Transformation**: None (Used raw percentile values).
* **Missing Values**: Applied **Listwise Deletion** to ensure consistent sample size ($n = N/A (Please check dataframe name)$).
* **Historical Benchmark ($\mu_0$)**: 65.0 (Based on historical average standards).

### 3. Data Cleaning
* **Process**: Removed all records with missing values in either target variable to maintain analysis integrity.

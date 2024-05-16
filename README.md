# Predict West Nile Virus in Mosquito Traps

## Project Overview

This project leveraged machine learning to strategically predict and manage the risk of West Nile Virus in Chicago by identifying mosquito traps that were likely to test positive. The objective was to efficiently allocate resources by minimising unnecessary testing and focusing efforts on high-risk areas, thus balancing cost-effectiveness with enhanced public safety measures. This approach not only helped in optimising the city's public health response but also in reducing the financial burden associated with widespread testing.

## Objectives

- **Maximise Recall**: Ensure most virus-carrying mosquitoes are detected to protect public health. High recall minimises the number of traps predicted to be negative for the virus when they are actually positive.
- **Maximise Precision**: Reduce unnecessary tests to save costs. High precision minimises the number of traps predicted to have the virus and tested, but that actually do not have the virus.

## Dataset

The dataset was sourced from the [Kaggle West Nile Virus Competition](https://www.kaggle.com/c/predict-west-nile-virus) and included weather data, mosquito trap data, and historical virus presence information.

## Methodology

1. **Data Preprocessing**:
   - Performed data cleaning and merged datasets to ensure consistency and accuracy.
   - Addressed missing values and encoded categorical variables to prepare for modelling.

2. **Feature Engineering**:
   - Extracted new features from date and weather data to enhance model inputs.
   - Used exploratory data analysis (EDA) to identify significant patterns and insights that guide the modeling process.

3. **Model Training**:
   - Applied several machine learning models including Logistic Regression, Random Forest, XGBoost, Gaussian Naive Bayes, Decision Trees, and AdaBoost to evaluate various predictive capabilities.
   - Utilised cross-validation and ROC AUC score for model evaluation and selection.

4. **Threshold Tuning**:
   - Adjusted decision thresholds to optimise the balance between recall and precision.
   - Determined the best thresholds for achieving desired True Positive Rates (TPR).

5. **Evaluation**:
   - Assessed model performance using confusion matrices and classification reports, providing a clear measurement of effectiveness.
   - Visualised ROC curves to precisely select the optimal thresholds for deployment.

## Model Performance and Cost Savings

In this project, a model was developed to predict which mosquito traps in Chicago are likely to have West Nile Virus. This helps the city decide where to focus its testing efforts, aiming to balance the need for public health safety with the goal of saving money. Here’s how the model performed with different settings:

## Cost Savings and Risks at Different Thresholds

| TPR (%) | Threshold (%)  | FPR (%) | Yearly Savings  |
|---------|----------------|---------|-----------------|
| 80.0    | 49.59          | 20.23   | $1,006,186.15   |
| 85.0    | 49.50          | 22.24   | $977,437.98     |
| 90.0    | 49.24          | 29.77   | $880,360.80     |
| 95.0    | 48.99          | 38.25   | $771,617.70     |
| 100.0   | 40.44          | 71.40   | $355,810.76     |

#### Key Metrics Explanation

- **TPR (%)**: True Positive Rate (Recall) - percentage of actual positives correctly identified. A higher TPR ensures more WNV-positive cases are detected, which is vital for public health as it means fewer cases are missed, reducing the risk of virus spread.
- **Threshold (%)**: The decision boundary percentage for predicting the presence of the virus. A lower threshold means the model is less stringent, leading to a higher TPR and catching more positive cases but also increasing false positives. A higher threshold is more stringent, reducing false positives but potentially missing more true positives.
- **FPR (%)**: False Positive Rate - percentage of negative cases incorrectly predicted as positive. This indicates the proportion of unnecessary tests, which impacts cost savings.
- **Yearly Savings**: Estimated annual savings by not testing traps predicted negative. This metric highlights the financial benefits of using the model to optimize testing and reduce unnecessary spending.

### Summary

The table highlights the trade-off between cost savings and the risk of missing positive cases at different thresholds. Lower thresholds increase the recall (TPR) and reduce the risk of missing positive cases but decrease savings. Higher thresholds enhance savings but increase the risk of missing positive cases. 

- At an 80% detection rate, the city could save about $1,006,186 a year, capturing most traps with the virus while also saving a significant amount of money. However, this setting also means that 20.23% of WNV-negative cases will be incorrectly predicted as positive, leading to unnecessary testing.
- A maximal detection rate of 100% means all potential cases are identified, with savings at $355,810. It's the safest option in terms of public health but offers the least savings, as 71.40% of the tests will be conducted unnecessarily.

Each setting represents a different balance between detecting the virus and saving costs, allowing the city to choose based on current public health priorities and budget considerations.

## Conclusion

The predictive model developed in this project has demonstrated significant potential for reducing costs and improving public health outcomes in Chicago's fight against the West Nile Virus. By identifying high-risk areas with greater accuracy, the city can allocate resources more effectively, focusing interventions where they are most needed. These findings suggest that strategic threshold settings can balance the dual objectives of cost-efficiency and public safety.

### Recommendation

Based on the model’s performance, we recommend that the City of Chicago aim for a True Positive Rate of 95%. This means that only if a specimen has an estimated probability greater than 48.99% of being WNV-positive, they should send it for testing. This threshold strikes a balance between minimizing false negatives and maximizing savings, with estimated annual savings of $771,617.70 despite 38.25% of tests being conducted unnecessarily.

### Risks and Assumptions

The results of this study depend on several key assumptions:
- **WNV Prevalence**: The prevalence of West Nile Virus will not change dramatically from year to year.
- **Geographic Distribution**: The distribution of WNV across Chicago will remain consistent.
- **Testing Costs**: The cost per lab test remains approximately $500.

These assumptions should be reviewed periodically to ensure the model's predictions remain valid. Adjustments may be needed if there are significant changes in these factors.

## Future Work

Recommendations for future work include testing additional predictive algorithms and using feature engineering techniques, such as Principal Component Analysis (PCA), to improve the balance between Precision and Recall.

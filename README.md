# Predict West Nile Virus in Mosquito Traps

## Project Overview

This project leverages machine learning to strategically predict and manage the risk of West Nile Virus in Chicago by identifying mosquito traps that are likely to test positive. Our objective is to efficiently allocate resources by minimising unnecessary testing and focusing efforts on high-risk areas, thus balancing cost-effectiveness with enhanced public safety measures. This approach not only helps in optimising the city's public health response but also in reducing the financial burden associated with widespread testing.

## Objectives

- **Maximise Recall**: Ensure most virus-carrying mosquitoes are detected to protect public health. High recall minimises the number of traps predicted to be negative for the virus when they are actually positive.
- **Maximise Precision**: Reduce unnecessary tests to save costs. High precision minimises the number of traps predicted to have the virus and tested, but that actually do not have the virus.

## Dataset

The dataset is sourced from the [Kaggle West Nile Virus Competition](https://www.kaggle.com/c/predict-west-nile-virus). It includes weather data, mosquito trap data, and historical virus presence information.

## Methodology

1. **Data Preprocessing**:
   - Performed data cleaning and merged datasets to ensure consistency and accuracy.
   - Addressed missing values and encoded categorical variables to prepare for modeling.

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

## Results

- **High Recall**: Effectively identified most virus-positive cases.
- **High Precision**: Minimised unnecessary tests, optimising cost savings.

## Results

In this project, we aimed to predict the presence of the West Nile Virus in mosquito traps to help the City of Chicago optimise its testing strategy, balancing cost savings and public health. We evaluated various thresholds to find the optimal balance between high recall and high precision.

#### Model Performance and Cost Savings

In this project, we developed a model to predict which mosquito traps in Chicago are likely to have West Nile Virus. This helps the city decide where to focus its testing efforts, aiming to balance the need for public health safety with the goal of saving money. Here’s how the model performed with different settings:

- **80% Detection Rate**: The city could save about $1,207,500 a year. This setting captures most traps with the virus while also saving a significant amount of money.
- **90% Detection Rate**: The savings drop to $1,056,500. This high detection rate ensures very few cases are missed.
- **100% Detection Rate**: Maximal detection means all potential cases are identified, with savings at $427,000. It's the safest option but offers the least savings.

Each setting represents a different balance between detecting the virus and saving costs, allowing the city to choose based on current public health priorities and budget considerations.

## Conclusion

This project demonstrates the potential of machine learning to enhance public health and economic efficiency through predictive modeling. The implemented models provide the City of Chicago with actionable insights to optimize their mosquito surveillance program, potentially reducing the spread of the West Nile Virus while saving on operational costs.

## Conclusion

The predictive model developed in this project has demonstrated significant potential for reducing costs and improving public health outcomes in Chicago's fight against the West Nile Virus. By identifying high-risk areas with greater accuracy, the city can allocate resources more effectively, focusing interventions where they are most needed. Our findings suggest that strategic threshold settings can balance the dual objectives of cost-efficiency and public safety.

## Future Work

We recommend testing additional predictive algorithms and using feature engineering techniques, such as Principal Component Analysis (PCA), to improve the balance between Precision and Recall.
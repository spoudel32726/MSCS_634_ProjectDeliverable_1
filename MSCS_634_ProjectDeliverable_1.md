# MSCS 634: Advanced Data Mining for Data-Driven Insights and Predictive Modeling
# Project Deliverable 1: Data Collection, Cleaning, and Exploration

## Dataset Selection and Justification

Selected Dataset: Wine Quality (White Wine Variant)
Source: UCI Machine Learning Repository (https://archive.ics.uci.edu/dataset/186/wine+quality)
Description: Physicochemical properties of white wines and their sensory quality ratings.
- Instances: 4898
- Attributes: 12 (11 continuous input features + 1 integer output: quality)
  - Features: fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol
  - Target: quality (score 0-10)
No missing values.

Justification:
- Meets criteria: >500 records, 8-10+ attributes.
- Real-world relevance: Applicable to quality prediction in food science.
- Suitable for future tasks: Regression, classification, clustering, etc.
- Note: Dataset downloaded as ZIP; code handles extraction.
## Insights from EDA and How They Guide Future Steps

From the EDA:
- **Distributions**: Quality scores are centered around 5-7, indicating class imbalance for classification tasks. Features like sulfur dioxide are skewed, suggesting normalization or transformation.
- **Outliers and Cleaning Choices**: Duplicates (937 removed) could bias models; outliers in chemical properties (removed via IQR) represent atypical wines, improving model generalization. Choices justified by focusing on typical data without excessive loss (~20-30% rows removed total).
- **Relationships**: Positive correlations (e.g., alcohol with quality) highlight key predictors. Negative correlations (e.g., volatile acidity) suggest quality detractors.
- **Guidance for Modeling**: Prioritize features with high corr to quality. For regression/classification, handle imbalance (e.g., SMOTE). Clustering may group by chemical profiles. Future steps: Feature engineering (scaling, binning).


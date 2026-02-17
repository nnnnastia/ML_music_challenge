## Vodafone Music Challenge
### Business Understanding

We build a binary classification model to predict whether a Vodafone subscriber will subscribe to Vodafone Music. The dataset includes 70,000 unique customers and ~460 behavioral, usage, and device-related features aggregated over three months.

The model supports targeted promotions: by identifying users with high likelihood of subscribing, Vodafone can optimize marketing budget and improve conversion rates. False Negatives (failing to identify a user who would subscribe) are especially costly as they represent lost revenue opportunities; hence metrics such as ROC-AUC, recall and F1 for the positive class are prioritized.

### Data Description

The dataset consists of:
- an `id` column for subscriber ID
- a binary `target` flag
- device characteristics (OS, device type, SIM count)
- usage statistics of services, apps, and URLs
- behavioral features over three months (suffixes m1, m2, m3)

Many features are sparse (counts = 0 for most users). Negative or missing values in usage features were converted to logical zeros; remaining missing numeric values were imputed using median.

### Baseline Dataset Preparation

To prepare the baseline dataset, we:
- removed duplicates
- replaced negative values with NaN
- filled usage/flag NaNs with 0
- filled other NaNs with median values

This cleaned dataset was then used for initial modeling with Logistic Regression, Random Forest, and Gradient Boosting approaches.

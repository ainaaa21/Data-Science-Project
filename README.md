# Predictive Consumer Preference Analysis for Clothing Brands in Malaysia

This project investigates consumer preferences and decision-making processes among Malaysian buyers, focusing on their selection between three popular apparel brands: **H&M**, **Uniqlo**, and **Brands Outlet**.

## Project Overview
The study employs a combination of qualitative and quantitative methods to uncover the key factors influencing consumer decisions, including:
- **Price**: The affordability and value-for-money perception.
- **Perceived Quality**: The durability and reliability of the products.
- **Style Preferences**: Alignment with current trends and personal fashion choices.
- **Brand Image**: The reputation and consumer perception of the brand.

To predict consumer choices, a **K-Nearest Neighbors (KNN)** predictive model was developed, leveraging these factors as key input variables.

## Data Collection
Data was collected via structured surveys targeting Malaysian consumers. The survey included demographic variables such as **age**, **gender**, and **income**, alongside questions designed to capture preferences and behaviors related to apparel shopping. This dataset forms the basis for identifying behavioral trends and developing actionable marketing strategies.

## Results
The study analyzed user preferences for H&M, Uniqlo, and Brand Outlet. To evaluate the performance of the predictive model, **K-Fold Cross-Validation (KF-CV)** with **k=5** was applied. The dataset was split into five folds, ensuring all data points were used for both training and testing during the validation process. 

The final model was chosen based on the iteration with the **highest testing accuracy**, ensuring robust performance on unseen data. Key results include:
- An **accuracy of 99.75%** during the training phase.
- A high accuracy of **90.0% on the testing dataset**.

These results demonstrate the KNN model's ability to generalize effectively and identify meaningful patterns in consumer preferences. The model’s high accuracy underscores its robustness, making it a valuable tool for deriving actionable insights in the clothing industry.

## Goals
This project aims to:
- **Understand consumer preferences** in the Malaysian retail market.
- **Develop predictive models** to forecast brand choices.
- **Provide actionable insights** for marketing and brand strategy optimization.

## Insights and Impact
This research offers significant value for businesses by enabling them to:
- **Tailor marketing strategies** to align with consumer preferences.
- **Enhance brand positioning** to appeal to specific demographics.
- **Stay competitive** in a dynamic retail environment by leveraging data-driven insights.

By identifying the factors that drive consumer decisions, this study equips retailers with the tools to better meet customer expectations and improve brand loyalty in a competitive market.

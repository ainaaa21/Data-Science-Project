# 👕 **Predictive Consumer Preference Analysis for Clothing Brands in Malaysia**  

## 📌 **Project Overview**  
This project investigates consumer preferences and decision-making processes among Malaysian buyers, focusing on their selection between three popular apparel brands: **H&M**, **Uniqlo**, and **Brands Outlet**.  

The study employs a combination of qualitative and quantitative methods to uncover key factors influencing consumer decisions, including:  
- **Price** 💰: Affordability and value-for-money perception.  
- **Perceived Quality** 🏆: Durability and reliability of products.  
- **Style Preferences** 👗: Alignment with fashion trends and personal choices.  
- **Brand Image** 🏢: Reputation and consumer perception of the brand.  

To predict consumer choices, a **K-Nearest Neighbors (KNN)** model was developed, leveraging these factors as input variables.  

---

## 📊 **Data Collection**  
The dataset was collected via structured surveys targeting Malaysian consumers. It includes demographic information such as **age, gender, and income**, along with responses related to shopping preferences. This dataset provides valuable insights into behavioral trends and serves as a foundation for data-driven marketing strategies.  

---

## 🤖 **Model Experimentation & Selection**  
To identify the best-performing model, **hyperparameter tuning** was conducted using different values of:  
- **p (1,2)**: Determines the Minkowski distance metric (Manhattan or Euclidean).  
- **n (1-10)**: Number of neighbors for classification.  

After testing multiple configurations, the optimal model was found to be:  
- **Best Model:** `p=1`, `n=4`  
- **Reason for Selection:** Achieved the **highest mean test accuracy of 94.2%**.  
- **Overfitting Check:** The gap between training accuracy (**95.75%**) and testing accuracy (**94.2%**) was minimal, indicating **low overfitting**.  
- **Standard Deviation:** **1.35**, showing stable performance across different K-Fold validation sets.  

---

## 📈 **Results & Model Performance**  
To ensure model reliability and robustness, **5-Fold Cross-Validation (KF-CV)** was applied, ensuring that all data points were used for both training and testing. The final model achieved:  
- 📌 **Training Accuracy:** **95.75%**  
- 📌 **Testing Accuracy:** **94.2%**  
- 📌 **Standard Deviation (1.35):** A low value suggests that model performance is stable across different data splits.  

These results demonstrate that the KNN model generalizes well and successfully identifies consumer preferences with high accuracy.  

---

## 🎯 **Project Goals**  
- 📌 **Understand consumer preferences** in the Malaysian retail market.  
- 📌 **Develop predictive models** to forecast brand choices.  
- 📌 **Provide actionable insights** for marketing and brand strategy optimization.  

---

## 📢 **Business Impact**  
This research provides **valuable insights** for businesses to:  
- 🎯 **Tailor marketing strategies** to match consumer behavior.  
- 🎯 **Enhance brand positioning** to attract the right target audience.  
- 🎯 **Stay competitive** by leveraging data-driven decision-making.  

🚀 _This project highlights how machine learning can empower businesses in understanding and predicting consumer behavior!_  

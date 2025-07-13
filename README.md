# 👕 Predictive Consumer Preference Analysis for Clothing Brands in Malaysia

## 📌 Project Overview  
This project explores how data science and machine learning techniques can be applied to analyze and predict **consumer brand preferences** in the Malaysian retail market. It simulates a real-world scenario where consumers choose between three popular apparel brands: **H&M**, **Uniqlo**, and **Brands Outlet**.

We aim to uncover decision factors such as:
- **Price** 💰
- **Perceived Quality** 🏆
- **Style Preferences** 👗
- **Brand Image** 🏢

---

## 1️⃣ Data Preparation & Exploration

### 📊 Data Collection  
A mock survey-style dataset was created, simulating real consumer profiles:
- Demographic info: **age**, **gender**, **income**
- Brand-related opinions: **price**, **quality**, **style**, **image**

### 🧹 Data Cleaning  
Performed in [Data Cleaning.ipynb](notebooks/Data%20Cleaning.ipynb) to address missing values and inconsistencies. Output stored in [Cleaned Dataset.csv](data/Cleaned%20Dataset.csv).

### 📉 Exploratory Data Analysis (EDA)  
Performed in [Data Analysis.ipynb](notebooks/Data%20Analysis.ipynb) to identify patterns and trends in consumer preferences.

#### 📊 Age vs Brand Preference
<p align="center">
  <img src="figure/analysis1.png" alt="Age vs Brand Preference" width="500"/>
</p>

**Insights:**
- 👕 **Brands Outlet** is the most preferred among teenagers aged **13–20**.
- 🧥 **H&M** shows strong preference among young adults aged **20–28**.
- 🧢 **Uniqlo** is preferred by both **13–20** and **20–28** groups, with balanced distribution.
- 👵 Older age groups (28–44) are less represented, suggesting the brands mainly appeal to younger consumers.

#### 📈 Monthly Expenses by Age and Gender
<p align="center">
  <img src="figure/analysis2.png" alt="Monthly Expenses by Age and Gender" width="600"/>
</p>

**Insights:**
- 📉 Most respondents are aged **15–25** with spending around **RM300–RM1000**.
- 👩‍🦰 Both genders show **similar spending trends**.
- 💸 Higher spenders (RM1500+) are older but less frequent.

#### 📎 Correlation: Monthly vs Clothes Expenses by Brand
<p align="center">
  <img src="figure/analysis3.png" alt="Monthly vs Clothes Expenses" width="600"/>
</p>

**Insights:**
- 📊 **Positive correlation** between overall monthly and clothing-specific expenses.
- 🟢 **Uniqlo** buyers spend more on clothing, often with higher income.
- 🔴 **Brands Outlet** suits lower spenders, hinting at price-sensitive market.

#### 🧾 Average Clothes Spending by Age Group
<p align="center">
  <img src="figure/analysis4.png" alt="Average Clothes Spending by Age Group" width="500"/>
</p>

**Insights:**
- 📈 Spending increases with age, peaking at **RM483.33** in the **37–44** category.
- 👶 Younger groups (13–20) spend less, likely due to **allowance limitations**.
- 🧓 Older consumers exhibit **higher purchasing power**.

#### 👚 Purchased Clothing Types by Brand
<p align="center">
  <img src="figure/analysis5.png" alt="Clothing Types by Brand" width="800"/>
</p>

**Insights:**
- 🏃‍♂️ **Brands Outlet** = **sportswear**
- 🧥 **H&M** = **casual wear**
- 👔 **Uniqlo** = **formal wear**
- 🔍 Clothing types align closely with **brand identity**.

#### 💵 Price Importance vs Employment Status
<p align="center">
  <img src="figure/analysis6.png" alt="Price Importance vs Employment" width="700"/>
</p>

**Insights:**
- 👨‍🎓 **Unemployed** consumers rate price as **very important**.
- 👩‍💼 **Employed** users consider price **less critical**.
- 💡 Indicates price sensitivity **varies with income**.

#### 🔥 Price Sensitivity vs Brand Preference (Heatmap)
<p align="center">
  <img src="figure/analysis7.png" alt="Heatmap: Brand vs Price Importance" width="500"/>
</p>

**Insights:**
- 💰 **H&M** and **Brands Outlet** attract **price-conscious** shoppers.
- 🌟 **Uniqlo** is favored by those who prioritize **quality over cost**.

#### 🛒 Shopping Preferences vs Clothing Type
<p align="center">
  <img src="figure/analysis8.png" alt="Shopping Type Preference" width="500"/>
</p>

**Insights:**
- 💻 **Online shoppers** lean toward **casual wear**.
- 🏬 **In-store buyers** purchase more **sportswear**.
- 🧠 Clothing type can influence **channel strategy** for retailers.

---

## 2️⃣ Predictive Modeling

### 🧪 Model Training & Testing  
A **K-Nearest Neighbors (KNN)** model was developed to classify user preference based on key survey features:
- **Input Features**: Price, Quality, Style, Brand Image, Age, Gender, Income  
- **Output Label**: Preferred Clothing Brand

To ensure reliable performance, the dataset was split into training and testing sets using a **5-Fold Cross-Validation** technique.  
This method helps evaluate the model’s generalizability by rotating test sets across 5 partitions—reducing bias and ensuring robustness across different subsets.

📁 [View K-Fold Split Data](data)

---

### 🔧 Hyperparameter Tuning  
To optimize the model, multiple combinations of KNN hyperparameters were tested:
- Distance metrics: `p = 1` (Manhattan), `p = 2` (Euclidean)  
- Number of neighbors: `n_neighbors` from 1 to 10  
- Process executed in [Model Experiment.ipynb](notebooks/Model%20Experiment.ipynb)

---

### ✅ Best Model Configuration  
Based on [K-Fold Experiment Result.csv](data/K-Fold%20Experiment%20Result.csv), the optimal model configuration is:

- `p = 1`, `n_neighbors = 4`  
- **Training Accuracy**: 95.75%  
- **Testing Accuracy**: 94.2%  
- **Standard Deviation**: 1.35  
- **Overfitting Check**: Minimal train-test gap suggests strong generalization

---

### 🧾 Final Model Evaluation  
Final classification logic was implemented in [Model Classification.ipynb](notebooks/Model%20Classification.ipynb).  
This notebook:
- Loads the **best-performing model parameters**
- Accepts **new data (in NumPy array format)**  
- Predicts **brand preference** based on unseen input  
- Demonstrates how the model could support **real-time prediction**

---

## 📈 Final Results  
Evaluated using 5-Fold Cross-Validation:
- ✅ **Training Accuracy**: 95.75%  
- ✅ **Testing Accuracy**: 94.2%  
- ✅ **Low Variance**: Standard deviation of 1.35 confirms consistent performance

---

## 🎯 Project Goals  
- ✅ Practice an end-to-end machine learning pipeline  
- ✅ Simulate consumer behavior using classification  
- ✅ Explore concepts like cross-validation and hyperparameter tuning  

---

## 📢 Potential Business Relevance *(Hypothetical)*  
If applied to real-world retail data, this analysis can:  
- 🎯 Improve brand marketing strategies by targeting age groups  
- 🎯 Personalize recommendations for fashion consumers  
- 🎯 Optimize product placement and promotion  

---

🚀 *This project demonstrates practical application of machine learning and EDA for simulating consumer decision behavior.*

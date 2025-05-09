# 👕 **Predictive Consumer Preference Analysis for Clothing Brands in Malaysia**

## 📌 Project Overview  
This project explores how data science and machine learning techniques can be applied to analyze and predict **consumer brand preferences** in the Malaysian retail market. It simulates a real-world scenario where consumers choose between three popular apparel brands: **H&M**, **Uniqlo**, and **Brands Outlet**.

The aim is to demonstrate understanding of predictive modeling by analyzing key decision factors, including:  
- **Price** 💰 – Affordability and value-for-money perception  
- **Perceived Quality** 🏆 – Durability and reliability of products  
- **Style Preferences** 👗 – Alignment with fashion trends and personal taste  
- **Brand Image** 🏢 – Reputation and consumer perception

A **K-Nearest Neighbors (KNN)** classifier was developed using these features to predict brand preferences.

---

## 📊 Data Collection  
A mock survey-style dataset was constructed to resemble real consumer data. It includes demographic attributes like **age**, **gender**, and **income**, along with consumer opinions on brand selection criteria. This simulated data serves as the foundation for applying machine learning classification methods.

---

## 🤖 Model Experimentation & Selection  
To assess model performance, **hyperparameter tuning** was performed by varying:  
- `p` (1, 2): Distance metric (Manhattan or Euclidean)  
- `n` (1–10): Number of nearest neighbors

### 🔍 Best Model Configuration  
- **p = 1**, **n = 4**  
- **Training Accuracy:** 95.75%  
- **Testing Accuracy:** 94.2%  
- **Standard Deviation (K-Fold):** 1.35  
- **Overfitting Check:** Small train-test accuracy gap indicates good generalization

---

## 📈 Results & Model Performance  
The model was evaluated using **5-Fold Cross-Validation** to ensure robustness:  
- ✅ **Training Accuracy:** 95.75%  
- ✅ **Testing Accuracy:** 94.2%  
- ✅ **Low Variance:** Standard deviation of 1.35 confirms consistent performance

---

## 🎯 Project Goals  
- 📌 Practice a complete machine learning pipeline (from data prep to evaluation)  
- 📌 Simulate consumer behavior analysis with classification models  
- 📌 Understand key ML concepts such as hyperparameter tuning and cross-validation

---

## 📢 Potential Business Relevance *(Hypothetical)*  
If applied in a real-world setting, this approach could:  
- 🎯 Help brands tailor marketing strategies to consumer behavior  
- 🎯 Guide data-driven brand positioning and outreach  
- 🎯 Improve decision-making in retail through customer insights

---

🚀 *This project showcases how machine learning can be used to simulate real-world applications and gain practical insights into data science workflows.*

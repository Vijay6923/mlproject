# 🎓 Student Performance Prediction using Machine Learning

This project analyzes and predicts student academic performance based on socio-demographic and preparatory attributes. It includes data exploration, visualization, preprocessing, training multiple regression models, and selecting the best-performing one based on key metrics.

---

## 📌 Problem Statement

Accurately predicting student performance can help educators identify students at risk of underperforming and take early action. By examining factors like gender, parental education, lunch type, and test preparation, we aim to forecast academic scores and uncover what really drives student success.

---

## 📂 Dataset Description

The dataset (`stud.csv`) contains the following columns:

| Column                     | Description                                 |
|---------------------------|---------------------------------------------|
| gender                    | Male or Female                              |
| race/ethnicity            | Categorical group assignment                |
| parental level of education | Highest education level achieved by parent |
| lunch                     | Standard or Free/Reduced lunch              |
| test preparation course   | Completed or None                           |
| math score                | Numeric score (0–100)                       |
| reading score             | Numeric score (0–100)                       |
| writing score             | Numeric score (0–100)                       |

---

## 📊 Exploratory Data Analysis (EDA)

Key insights from the data:

- Students who completed a **test preparation course** scored higher in all three subjects.
- **Females outperformed males** in reading and writing.
- **Reading and writing scores** are highly correlated.
- **Parental education** level is moderately linked to student performance.

Visuals include histograms, boxplots, and correlation heatmaps to support these findings.

---

## 🧹 Data Preprocessing

Steps taken before model training:

- Verified data cleanliness (no missing values)
- Converted categorical variables using label encoding
- Normalized target scores where necessary
- Split data into training and test sets (80/20 split)

---

## 🤖 Model Building

The following regression models were trained and evaluated:

- Linear Regression
- Ridge & Lasso Regression
- K-Nearest Neighbors Regressor
- Decision Tree Regressor
- Random Forest Regressor
- AdaBoost Regressor
- CatBoost Regressor

---

## 📈 Model Evaluation

All models were evaluated using R² Score, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE). Here's a summary:

| Model               | R² Score | MAE   | RMSE  |
|--------------------|----------|-------|-------|
| Linear Regression  | 0.85     | 3.21  | 4.12  |
| Random Forest      | 0.91     | 2.34  | 3.28  |
| CatBoost           | 0.92     | 2.18  | 3.10  |

**CatBoost Regressor** performed best and was selected as the final model.

---

## ✅ Conclusion

- Features like test preparation, gender, and parental education significantly influence academic performance.
- CatBoost provided the highest accuracy and lowest error.
- This model can be integrated into early intervention systems for academic support.

---

## 🚀 Future Work

- Integrate SHAP or LIME for feature explainability
- Deploy model using Streamlit or Gradio
- Explore deep learning methods like TabNet or MLP
- Collect and train on more diverse datasets

---

## 🛠 How to Run This Project

```bash
# Install required libraries
pip install -r requirements.txt

# Run notebooks
jupyter notebook EDA_STUDENT_PERFORMANCE.ipynb
jupyter notebook model_training.ipynb


📁 Project Structure

.
├── data/
│   └── stud.csv
├── EDA_STUDENT_PERFORMANCE.ipynb
├── model_training.ipynb
├── README.md
└── requirements.txt


🙋‍♂️ Author

Vijay


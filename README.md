# ⚽ Premier League Match Prediction using Machine Learning

This project uses machine learning to predict the outcomes of Premier League football matches. It leverages historical match data, engineered features, and a **Random Forest Classifier** to determine whether a team will win its upcoming match.

## 📂 Project Overview

- **Goal**: Predict whether a team wins (`W`) a match.
- **Algorithm**: Random Forest Classifier.
- **Dataset**: Historical Premier League match data (`matches.csv`).
- **Target Variable**: `target` → 1 if the team won, 0 otherwise.
- **Performance Metrics**: Accuracy, Precision, and Confusion Matrix.

## 🚀 Features & Workflow

### ✅ 1. Data Preprocessing
- Convert date column, encode venue and opponent, extract time & weekday.
- Create the target variable indicating match win (1) or not (0).

### ✅ 2. Train/Test Split
- Train data: Matches before **2022-01-01**
- Test data: Matches after **2022-01-01**
- Features used: `venue_code`, `opp_code`, `hour`, `day_code`

### ✅ 3. Model Training
A Random Forest Classifier is trained to predict match outcomes.

### ✅ 4. Evaluation
- Accuracy Score
- Precision Score (~47%)
- Confusion Matrix shows true and false predictions.

## 📊 Advanced Feature Engineering
Rolling averages (last 3 matches) for stats such as:
- Goals For/Against, Shots, Shots on Target, Distance Covered, Fouls, Penalties, etc.

These improve predictive performance by capturing team form.

## 📁 File Structure

```
├── matches.csv         
├── notebook.ipynb      
├── README.md           
```

## 🛠️ Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Jupyter Notebook / Google Colab

## ✅ How to Run
1. Install dependencies:
   ```bash
   pip install pandas scikit-learn
   ```
2. Place `matches.csv` in the project folder.
3. Run the notebook or Python script.

## 📌 Future Improvements
- Hyperparameter tuning
- Add XGBoost/LightGBM models
- Use betting odds as features
- Deploy with Flask/Streamlit

## 🙌 Acknowledgements
Built for educational purposes to explore machine learning in sports analytics.

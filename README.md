# 🏏 Cricket Match Outcome Prediction | Day 27 – 30 Days Data Science Challenge

## 📌 Project Overview

This project focuses on predicting the outcome of IPL cricket matches using historical match-level data.

The goal is to build a machine learning model that predicts whether **Team1 wins the match** based on match conditions such as toss decision, venue, season, and other contextual features.

---

## 📊 Dataset Information

The dataset contains historical IPL match data with the following columns:

- id
- season
- city
- date
- team1
- team2
- toss_winner
- toss_decision
- result
- dl_applied
- winner
- win_by_runs
- win_by_wickets
- player_of_match
- venue
- umpire1
- umpire2

---

## 🎯 Problem Statement

Predict:

`team1_win`  
- 1 → Team1 wins  
- 0 → Team1 loses  

This is a **binary classification problem**.

---

## 🧹 Data Preprocessing

### 1️⃣ Feature Engineering

Created new features:

- `team1_win`
- `toss_match_win`
- Extracted season trends
- Venue-based win insights

### 2️⃣ Removed Data Leakage Columns

The following columns were dropped to prevent leakage:

- winner
- win_by_runs
- win_by_wickets
- result
- player_of_match

---

## 📊 Exploratory Data Analysis (EDA)

### 🔹 Toss Decision
- Majority teams choose to field first.
- Toss advantage is not strongly correlated with winning (~42.8%).

### 🔹 Venue Analysis
Top venues:
- M Chinnaswamy Stadium
- Eden Gardens
- Feroz Shah Kotla
- Wankhede Stadium

Venue plays a moderate role in match outcome.

### 🔹 Season Trends
Team1 win probability fluctuates across seasons.
No strong seasonal dominance observed.

---

## 🤖 Model Building

### Model 1: Logistic Regression
Accuracy: **53.6%**

### Model 2: Random Forest
Accuracy: **59.2%**

Confusion Matrix:

| Actual / Predicted | 0 | 1 |
|--------------------|---|---|
| 0 | 48 | 27 |
| 1 | 24 | 26 |

---

## 📈 Model Insights

- Cricket matches are inherently unpredictable.
- Contextual features alone give limited predictive power.
- Random Forest performed better than Logistic Regression.
- Accuracy remains near 60%, reflecting real-world uncertainty.

---

## 🚀 Improvements for Future Work

- Include ball-by-ball data
- Add team strength metrics
- Player performance features
- Recent form indicators
- Head-to-head statistics
- Venue-specific win history

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn

---

## 📌 Key Learning

Cricket outcome prediction is complex and highly stochastic.  
Even advanced models struggle without deep contextual and player-level features.

---

## 📎 Conclusion

This project demonstrates:
- Proper handling of data leakage
- Feature engineering for sports analytics
- Realistic expectations in predictive modeling
- Model comparison and evaluation

Accuracy ≈ 59% reflects real-world sports uncertainty — which makes this a practical and honest ML project.

---

👨‍💻 Built as part of:
#30DaysDataScienceChallenge

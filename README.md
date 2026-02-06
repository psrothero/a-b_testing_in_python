Here is the raw Markdown code for your README.md. You can copy and paste this directly into your GitHub editor.

Markdown
# Optimising User Retention: Cookie Cats A/B Test & Churn Prediction

## 📌 Project Overview
This project investigates the impact of moving the first "gate" in the mobile puzzle game **Cookie Cats** from Level 30 to Level 40. By combining **Statistical Bootstrapping** and **Logistic Regression**, I evaluated how this change affects player retention and built a predictive model to identify users at risk of churning.

## Tech Stack
* **Language:** Python 3.13
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn
* **Key Methods:** Bootstrap Resampling, Logistic Regression, Hypothesis Testing

## Phase 1: Statistical Hypothesis Testing
I conducted a robust A/B test to determine the impact of gate placement on 7-day retention.

* **Null Hypothesis ($H_0$):** There is no significant difference in retention between Gate 30 and Gate 40 ($Ret_{30} = Ret_{40}$).
* **Alternative Hypothesis ($H_1$):** There is a statistically significant difference in retention ($Ret_{30} \neq Ret_{40}$).
* **Methodology:** 10,000 Bootstrap iterations to estimate the sampling distribution of the difference in means.
* **Findings:** There is a **99.9% probability** that Day-7 retention is higher when the gate remains at **Level 30**. 

## Phase 2: Predictive Modelling (Churn Risk)
I developed a Logistic Regression model to predict player retention based on version and early-game engagement.

* **Model Accuracy:** 87.14%
* **F1-Score:** 55.42% 
* **Feature Importance (Odds Ratios):**
    * **Gate Version (0.94):** Moving the gate to Level 40 reduces the odds of retention by **6%**.
    * **Game Rounds (1.02):** Every additional round played increases the odds of retention by **2%**.

## Key Insights
1. **The "Gate 30" Advantage:** Forcing a break at Level 30 aligns better with player psychology (Hedonic Adaptation), preventing boredom and increasing long-term retention.
2. **Engagement is King:** The number of rounds played is the strongest predictor of whether a player will stay, outweighing the impact of the gate version itself.
3. **Operational Utility:** While the model deals with class imbalance, it serves as an effective tool for identifying **high-risk churners** for targeted re-engagement campaigns.

## Business Recommendations
* **Maintain the Status Quo:** Do not move the gate to Level 40; the data indicates a clear negative impact on user retention.
* **Early Hook Strategy:** Implement features that encourage players to complete at least 20 rounds within their first session to significantly boost the probability of them returning.

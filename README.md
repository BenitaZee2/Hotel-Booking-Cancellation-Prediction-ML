# Hotel Booking Cancellation Prediction (Python / ML)

A predictive model to determine hotel booking cancellation status, built to help a hotel reduce revenue loss and improve resource planning.

## Business Problem
Hotel Haven needed a way to predict which bookings were likely to be cancelled, understand the behavioral and structural factors driving cancellations, and use that insight to improve customer retention and operational planning.

## Aim
- Develop a predictive model to determine booking cancellation status
- Identify the patterns and factors most strongly linked to cancellations
- Support data-driven decisions on customer retention and resource allocation
- Reduce cancellation rates and improve operational efficiency

## Approach

**1. Data Investigation & Cleaning**
- Numerical and categorical statistical analysis of the raw booking dataset
- Data cleaning and structural review of the full dataset

**2. Exploratory Data Analysis**
- Cancellation rate found to be 33% of all bookings — high enough to materially affect revenue
- Feature engineering on Duration and Season fields
- Correlation analysis across numerical features
- Categorical distribution analysis across market segment, room type, meal plan, and season
- Outlier detection and treatment using histograms and boxplots

**3. Feature Engineering & Preprocessing**
- Categorical variable encoding
- Numerical feature scaling
- Class imbalance handled using SMOTE

**4. Modeling**
Multiple classification models trained and compared:
- Logistic Regression (baseline)
- Random Forest (advanced)
- Gradient Boosting
- AdaBoost
- SVC
- K-Nearest Neighbors
- Decision Tree
- XGBoost

Model evaluation included confusion matrices for each classifier and a comparative heatmap, followed by hyperparameter tuning and final model evaluation.

## Key Insights
- **Lead time** has the strongest positive correlation with cancellation — the further in advance a booking is made, the more likely it is to be cancelled
- **Repeated guests** cancel less than first-time guests
- **Special requests** show a slight negative correlation with cancellation — guests with specific needs tend to be more committed
- **Booking channel matters**: bookings made through intermediaries (online travel agencies) show the highest cancellation rates, while walk-ins and direct offline bookings are far less likely to cancel
- Cancelled bookings show a slightly higher median average price and greater price variability
- Meal plan selection was not a strong predictor of cancellation

## Strategic Insight
Cancellation risk is driven by **commitment, not volume**. Guests who commit financially or structurally (meal plans, corporate travel, standard rooms) are far less likely to cancel than those booking speculatively far in advance through third-party channels.

## Recommendations
- Deploy the Random Forest model to flag high-risk bookings in real time — particularly those with long lead times, high prices, and low commitment indicators
- Build targeted retention strategies for guests flagged as high cancellation risk
- Shift decision-making from reactive to proactive using the model's outputs to guide operational and revenue planning

## Tools
Python — pandas, matplotlib/seaborn, scikit-learn, XGBoost, imbalanced-learn (SMOTE)

## Skills Demonstrated
Exploratory data analysis · feature engineering · handling class imbalance · classification modeling · model evaluation & comparison · hyperparameter tuning · business-focused insight communication

# Linear_Regression_Taxi_Fare_Prediction-Python
This project aims predicts taxi fares in Chicago using historical trip data.

🗂 Dataset
Source: chicago_taxi_train.csv

Size: 31,694 rows × 18 columns

Target Variable: FARE (taxi fare in USD)

🧹 Data Cleaning & Feature Selection
Identified missing values in several columns (PICKUP_CENSUS_TRACT, DROPOFF_CENSUS_TRACT, etc.)

Selected 6 relevant features for analysis:

TRIP_MILES (trip distance in miles)

TRIP_SECONDS (trip duration in seconds)

FARE (target variable)

TIP_RATE (tip percentage)

PAYMENT_TYPE (payment method)

COMPANY (taxi company)

No missing values in the selected feature subset

📊 Exploratory Data Analysis (EDA)
Statistical Summary
Maximum Fare: $159.25

Mean Distance: 8.29 miles

Most Frequent Payment Type: Credit Card (14,142 trips)

Number of Taxi Companies: 31

Most Common Company: Flash Cab (7,887 trips)

Correlation Analysis
The correlation matrix revealed:

TRIP_MILES ↔ FARE: 0.975 (very strong positive correlation)

TRIP_SECONDS ↔ FARE: 0.830 (strong positive correlation)

TIP_RATE ↔ FARE: -0.071 (weak negative correlation)

TRIP_MILES ↔ TRIP_SECONDS: 0.801 (strong correlation)

Key Insights
Distance is the strongest predictor of fare (0.975 correlation)

Trip duration is also highly correlated with fare (0.830)

Tip rate shows little correlation with fare amount

The data shows natural relationships expected in taxi pricing

Data Visualization
Used plotly.express.scatter_matrix to visualize relationships between FARE, TRIP_MILES, and TRIP_SECONDS

Created pairwise scatter plots showing clear linear relationships

🛠 Tools & Libraries Used
pandas – Data manipulation and analysis

numpy – Numerical operations

matplotlib – Basic plotting

plotly – Interactive visualizations

keras – Imported (but not yet used for modeling)

📈 Next Steps (For Future Development)
This notebook establishes the foundation for building a predictive model. Next steps would include:

Data Preparation:

Train/test split

Feature scaling/normalization

Handling categorical variables (PAYMENT_TYPE, COMPANY)

Model Building:

Implement linear regression model

Consider additional features (time of day, day of week)

Evaluate model performance

Model Evaluation:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R² score

🎯 Key Findings
Fare Range: $3.25 – $159.25

Mean Trip Distance: 8.29 miles

Most Common Payment: Credit Card (44.6% of trips)

Top Company: Flash Cab (24.9% of trips)

Primary Predictors: Trip miles and trip seconds are highly correlated with fare

# Zillow-Data_Time-Series-Forecasting
# Project Structure
## Overview 
This project analyzes housing market trends across selected western U.S. states, forecasts future home values in Oregon using time series models, and presents key insights through an interactive Tableau Story.
## Part 1: Data Preparation and Exploratory Analysis
### Objectives
- Load and preprocess the housing dataset.
- Transform the data into a time series format.
- Prepare a Tableau-ready dataset.
-  Analyze yearly home value trends by state.
### Tasks
1. Load the CSV dataset.
2. Convert the dataset from wide format to long format.
3. Rename columns to:
   - Date
   - Home Value
4. Convert the Date column to datetime format and set it as the index.
5. Filter data for:
     - States: CA, WA, OR, AZ, NV
     - Years: 2010–2020
6. Save the processed dataset as:
     - `Data/data-for-tableau.csv`
7. Calculate yearly mean home values by state.
8. Create a line chart comparing annual home value trends across states.
   <img width="859" height="1142" alt="تنزيل (2)" src="https://github.com/user-attachments/assets/7664bca2-7066-4151-8170-0bedbb9d44c8" />

---
## Part 2: Time Series Forecasting for Oregon
### Objectives
- Forecast Oregon's average home values for the next 12 months.
- Compare manual and automated forecasting approaches.
- Select the best-performing model.
### Tasks
1. Filter Oregon (OR) data from 2000–2018.
2. Create a monthly mean home value time series.
3. Handle missing values.
4. Decompose the series to identify trend and seasonality.
5. Assess stationarity and apply differencing if necessary.
6. Use ACF and PACF plots to determine initial model orders.
7. Split the data into training and testing sets.
8. Fit a manual ARIMA/SARIMA model.
9. Evaluate model performance using:
      - MAE51   - MSE  - RMSE  - R²  - MAPE
11. Tune models using Auto ARIMA.
12. Compare models and select the final model.
13. Generate 12-month future forecasts.
14. Visualize forecasts and summarize:
   - Final forecasted home value
   - Percentage change over the forecast period
<img width="868" height="393" alt="تنزيل (1)" src="https://github.com/user-attachments/assets/df978b2c-efae-4107-80f4-3f3657881577" />

     ----
## Part 3: Data Visualization with Tableau
### Objectives
- Build an interactive Tableau Story to communicate housing market insights.
### Story Points
#### Story 1: Median Home Value by Location
- Bar chart of median home values by State, County, and ZIP Code.
- Display only the Top 20 most expensive ZIP codes.
- Color by County Name.

  <img width="1448" height="592" alt="Screenshot 2026-07-18 113936" src="https://github.com/user-attachments/assets/e47494b5-554a-453f-89b3-f5c0bd1281af" />

#### Story 2: Home Value Growth by State
- Line chart showing percentage change in home values from 2010–2020.
- Compare trends across CA, WA, OR, AZ, and NV.
- Include annotation identifying the state with the largest increase.
  <img width="1446" height="765" alt="Screenshot 2026-07-18 114108" src="https://github.com/user-attachments/assets/ca566da2-f1c9-49ab-a5b4-d02b0d020576" />

#### Story 3: Most Expensive ZIP Codes82- Highlight table of the Top 20 most expensive ZIP codes.
- Filtered to December 2020.
- Display:
- State
- County Name
- City
- ZIP Code
- Median Home Value
  <img width="1452" height="588" alt="Screenshot 2026-07-18 114131" src="https://github.com/user-attachments/assets/8fbaef1d-85bc-4476-97ab-b4a0681dab4b" />

#### Story 4: Geographic Distribution of Home Values
  - Choropleth map of median home values by ZIP Code.
  - Filtered to December 2020.
  - Dark map style with County and City tooltips.
    <img width="1426" height="746" alt="Screenshot 2026-07-18 114251" src="https://github.com/user-attachments/assets/22958878-f5b2-4ae4-80e9-e1ddc36cfc48" />

### Deliverables
  - Tableau Public Story containing all four visualizations.
  - Appropriate captions for each story point.
  - Shareable Tableau Public link included in the notebook under:
  ```markdown
  # Tableau Workbook
https://public.tableau.com/views/Zillowhomevalues/differenceinmedianHomeValueperstate?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

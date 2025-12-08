**First Commit**

# Taxi Fare Regression Modeling - Automatidata (PACE Strategy)

This project analyzes NYC Taxi & Limousine Commission (TLC) data to build a regression model that predicts taxi fare amounts. The analysis follows the **PACE Strategy** (Plan → Analyze → Construct → Execute)

---

# Plan

## Project Goal 
Automatidata has been approached by the NYC TLC to support the development of an app that predicts taxi fares for riders **before** they take a trip. The goal is to build a regression model that estimates fare amounts using trip-related variables.

## Business Task 
- Compute descriptive statistics
- Build a regression model for fare prediction
- Prepare an executive summary for non-technical stakeholders


# Key Questions 
- What variables influence taxi fares the most?
- How well can a regression model predict fare amounts?
-What insights should the TLC consier for their fare-estimation app?


## Stakeholders 
- **TLC Operations Manager** (client)
- **Automatidata Data Team** (Me)
- **App Development Team** (uses the model in production)

---

# ANALYZE

## Dataset Description  
This dataset includes:  
| Feature | Description |
|--------|-------------|
| VendorID | Taxi provider ID |
| tpep_pickup_datetime | Trip start time |
| tpep_dropoff_datetime | Trip end time |
| passenger_count | Number of riders |
| trip_distance | Distance (miles) |
| RatecodeID | Ride rate category |
| payment_type | 1=Credit, 2=Cash, etc. |
| fare_amount | Base fare |
| extra, mta_tax, improvement_surcharge | Flat surcharges |
| tip_amount | Customer tip |
| tolls_amount | Tolls added |
| total_amount | Final trip cost |

##  Data Preparation  
- Removed missing or invalid entries  
- Encoded variables  
- Analyzed outliers  
- Checked distributions  
- Created initial visualizations  

---

# CONSTRUCT

## Regression Modeling  
Models built: 
- Multiple Linear Regression (final model)

Variables used:
- passenger_count  
- fare_amount
- mean_distance
- mean_duration
- rush_hour

---

# EVALUATE

##  Model Evaluation Metrics   
- **R²:** 0.89 
- **MSE** 12.10 
- **RMSE:** 3.47 
- **MAE:** 1.99  

## Residual Insights  
- The distribution of the residuals is approximately normal 
    and has a mean of -0.015  
- No major regression violations  


## Strengths  
- Highly interpretable  
- Strong predictive power from ride_duration  

## Evaluation Conclusion  
The model performs strongly and is reliable enough for fare estimation. Adding more features would further enhance performance.

---

# EXECUTE

## Executive Summary  
The feature with the greatest effect on fare amount was ride duration,  which was not unexpected. The model revealed a mean increase of $7 for each additional minute, however, this is not a reliable benchmark due to high correlation between some features. 

Request additional data from under-represented itineraries. 

The New York City Taxi and Limousine commission can use these findings to create an app that allows users (TLC riders) to see the estimated fare before their ride begins.

The model provides a generally strong and reliable fare prediction that can be used in downstream modeling efforts.



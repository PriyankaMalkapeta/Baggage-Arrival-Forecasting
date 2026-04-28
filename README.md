#  Baggage Arrival Forecasting System

Machine Learning project focused on predicting baggage arrival/check-in timing before scheduled flight departures using large-scale airline operational data.

This solution helps airports and airlines improve:

- Workforce planning  
- Baggage handling efficiency  
- Check-in resource allocation  
- Peak travel staffing decisions  
- Operational forecasting

---

# 📌 Project Overview

Efficient baggage operations are critical for airport performance and customer satisfaction.

Passengers check in bags at different times depending on:

- Flight type (Domestic vs International)
- Flight distance (Short-haul vs Long-haul)
- Departure time of day
- Day of week
- Peak travel seasons

This project uses Machine Learning to forecast **when bags arrive before departure**, enabling better planning and reduced congestion.

---

# 📊 Dataset Summary

- Source: Confidential airline operational dataset  
- Airline Context: Major U.S. carrier  
- Records: **50,968,404+ observations**
- Features: **33 variables**
- Time Period: **Jan 2024 – Dec 2024**

Examples of features:

- Flight departure time
- Flight distance
- Domestic / International indicator
- Aircraft type
- Weekly / daily frequency
- Bag scan timestamps
- Route scheduling patterns

> ⚠️ Original dataset is confidential and not included in this repository.

---

# 🎯 Business Problem

Airports need to predict baggage inflow before departures to:

- Assign staff efficiently
- Reduce baggage bottlenecks
- Improve conveyor / pier utilization
- Handle peak season surges
- Improve on-time baggage loading

---

# ⚙️ Tech Stack

## Languages
- Python

## Libraries
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- Matplotlib
- Seaborn
- SciPy

## Environment
- Jupyter Notebook

---

# 🧹 Data Engineering & Preprocessing

Performed:

- Datetime parsing
- Feature engineering
- Target variable creation
- Missing value handling
- Outlier removal (IQR Method)
- Encoding categorical variables
- Train/test split
- Scaling where required

## Target Variable

`BAG_SCAN_TO_DEP_MIN`

Minutes between baggage scan time and scheduled flight departure.

---

# 🤖 Models Built

## 1. Linear Regression
Baseline model.

## 2. Random Forest Regressor
Best performing model.

## 3. Multi-Layer Perceptron (MLP Regressor)

## 4. LightGBM

# 📈 Key Insights

## Peak Bag Arrival Window

Most bags arrive:

**80–120 minutes before departure**

## International Flights

Passengers on international flights check bags earlier than domestic travelers.

## Long-Haul Flights

Long-haul baggage tends to arrive earlier than short-haul.

## Peak Seasons

Peak travel periods account for:

**63.6% of baggage volume**

## Last-Minute Check-ins

Only:

**4.7% of bags arrive in final 30 minutes**

---

# 📊 Visual Analytics Included

- Histogram of baggage arrival times
- Domestic vs International comparison
- Weekday vs Weekend behavior
- Seasonal peak demand charts
- Feature importance
- Correlation heatmap
- Model comparison charts

---

# 💡 Operational Recommendations

Based on findings:

## Staffing

Increase staffing during:

- 80–120 minute pre-departure window
- Peak travel months
- International departure banks

## Resource Planning

Allocate belts / piers dynamically using forecasted bag volume.

## Predictive Scheduling

Use ML outputs to optimize labor shifts.

---

# 📁 Repository Structure

```text
baggage-arrival-prediction/
│
├── FINAL_CODE_OF_AA.ipynb
├── Predicting Baggage Arrival.pdf
├── README.md
├── requirements.txt
└── images/

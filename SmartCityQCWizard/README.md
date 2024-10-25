# Smart City QC Wizard Challenge: Simulating Overtourism and Weather Alerts in Cagliari

This repository contains the code and models developed for the **Smart City QC Wizard Challenge**. The objective was to create a system capable of predicting overtourism events and environmental hazards in Cagliari, Italy, using Quantum Machine Learning (QML) and simulations. 

## Team Members
0. Name: email|discord_id

1. Epameinondas Douros: EpaDouros@gmail.com|352580588655476765
2. Konstantinos Dalampekis: konstantinosdalampekis@gmail.com|762989571487039498
3. Aggelos Kastrinellis: angelkastr@gmail.com|325639468684017665
4. Evripidis Koutsoumpas: ekoutsioumpas@gmail.com

## Table of Contents
- [Project Overview](#project-overview)
- [Initial Data Analysis](#initial-data-analysis)
- [Solution 1: Simulating Overtourism](#solution-1-simulating-overtourism)
- [Solution 2: Predicting Weather Alerts with QML](#solution-2-predicting-weather-alerts-with-qml)
- [Model Development](#model-development)
- [Results](#results)
- [How to Run the Code](#how-to-run-the-code)
- [Future Work](#future-work)

## Project Overview

Overtourism and environmental hazards pose significant challenges to cities, affecting infrastructure, environment, and residents' well-being. This project aims to provide solutions for predicting these events in Cagliari using Quantum Machine Learning (QML) and simulations based on available data and insights from research papers.

## Initial Data Analysis

### Data Challenges
Upon initial analysis, we found that the dataset provided contained several missing values, and many variables lacked strong correlations that could directly explain overtourism or environmental hazards. Due to these limitations:
- We could not build a strong argument or pattern directly from the raw data.
- The missing values made it difficult to compose a reliable predictive model solely based on the provided datasets.

### Devised Solutions
Given these challenges, we developed two complementary approaches:
1. **Simulation-Based Solution**: To address the overtourism problem in Cagliari, we designed a simulation model based on information from research papers and historical insights into tourism patterns. This approach allowed us to model potential overtourism scenarios and assess their impact.
2. **Raw Data with QML for Weather Alerts**: Despite the data limitations, we used the available raw data to develop a Quantum Machine Learning (QML) model. This model focused on predicting weather-related alert conditions, which might influence or correlate with overtourism events and environmental hazards.

## Solution 1: Simulating Overtourism (combined_dataset__analysis (3).ipynb)

### File -> combined_dataset__analysis (3).ipynb

### Simulated Data
Due to the lack of comprehensive real-world data, we created a simulated dataset reflecting various factors influencing tourism and environmental conditions:
- **Tourism Metrics**: Tourist attendance, cruise ship arrivals, hotel occupancy, and beach occupancy rates.
- **Event Influence**: Major events like the Saint Efisio festival, concerts, and cultural festivals.
- **Environmental Metrics**: Air pollution levels (PM10, PM2.5, CO, NO2), noise levels, and water/energy usage.
- **Weather Conditions**: Temperature, wind speed, and humidity.

### Threshold Definitions
We established thresholds to classify overtourism and environmental hazards:
- **Overtourism**:
  - Tourist attendance > 3000
  - Cruise ship arrivals > 4 per day
  - Hotel occupancy rate > 85%
- **Environmental Hazard**:
  - PM10 levels > 60 µg/m³
  - Noise level > 80 dB

### 30-Day Forecast
The QRNN and QLSTM models were used to forecast overtourism and environmental hazards for the next 30 days using the recursive forecasting method.

## Solution 2: Predicting Weather Alerts with QML

Using the raw data, we focused on predicting weather alert conditions as a proxy for environmental risk. By leveraging QML:
- We developed models that used available metrics such as temperature, wind speed, and air pollution levels to predict hazardous conditions.
- This approach allowed us to test the effectiveness of quantum models in identifying patterns and alerting city planners about potential environmental risks that could be correlated with overtourism.

### 1.File -> Total_Analysis_Weather_QVC_2.ipynb

This Jupyter notebook focuses on analyzing weather data and exploring potential correlations between different environmental variables. Here's a brief overview of the workflow and insights:

Data Analysis:

We initially explored and combined various datasets to investigate correlations between different weather and environmental factors.
After comprehensive analysis, it was observed that there were limited significant correlations between the variables.
Weather Classification:

The focus shifted towards predicting weather conditions by classifying the weather status based on specific conditions like temperature, wind speed, and other relevant metrics.
This classification allows for a better understanding of future weather conditions based on existing data, aiding in weather forecasting.

### 2.File -> Unique_Attendance_QLSTM.ipynb

Data Preprocessing:

Multiple datasets are loaded, each representing attendance data for different periods.
Initial preprocessing steps include data cleaning, handling missing values, and merging datasets to form a unified structure.
The analysis focuses on identifying unique areas and metrics related to attendance using distinct categories such as areaAnalisi.
Exploratory Data Analysis (EDA):

Visualizations are generated to explore the trends in attendance, looking at how metrics change over time.
Statistical summaries and plots are used to identify key patterns, distributions, and potential outliers in the data.
Correlation analysis is performed to see if any relationships exist between variables and attendance behavior.
Predictive Modeling with QLSTM:

The analysis includes building predictive models to forecast attendance using historical data.
A specialized model like QLSTM (Quantum Long Short-Term Memory) may be applied to predict attendance trends, leveraging its strength in handling time-series data.
Model evaluation includes accuracy, error metrics, and validation of predictions against actual data to ensure reliability.
Result Interpretation:

The outcomes of the predictive analysis are visualized and compared with historical attendance trends.
Insights are drawn about what factors impact attendance and how future trends might behave.
Recommendations based on the analysis are suggested, offering guidance for improving attendance forecasting. 

## Model Development

### Quantum Recurrent Neural Network (QRNN)
We implemented a **QRNN** using PennyLane and Qiskit:
- **Quantum Circuits**: Parameterized quantum circuits were used to encode and process sequential data, leveraging quantum entanglement and superposition.
- **Training**: The QRNN was trained using gradient descent to minimize errors in predicting both overtourism events and weather alert conditions.

### Quantum Long Short-Term Memory (QLSTM)
To handle long-term dependencies more effectively, we developed a **QLSTM** model:
- The QLSTM processed time-series sequences using quantum gates simulating classical LSTM memory cells, capturing long-term patterns in the data.

### Recursive Forecasting
Both models were employed in a recursive forecasting approach:
- Starting from the most recent known data, the models predicted future values iteratively for the next 30 days, using the output of each prediction as input for the next.

## Results

### Simulation-Based Predictions
The simulation model successfully demonstrated potential overtourism patterns in Cagliari based on research data, highlighting peak periods and environmental risk zones. The model provided insights into managing overtourism more effectively.

### QML-Based Weather Alerts
The QML model, despite the limitations of the raw data, successfully predicted weather alert conditions, showing potential for integration with real-time data to enhance environmental monitoring systems.

## How to Run the Code

1. **Install Dependencies**:
   Ensure the necessary Python libraries are installed:
   ```bash
   pip install pennylane qiskit scikit-learn matplotlib numpy pandas

## Future Work
We aim to gather more accurate and comprehensive data to refine our simulation model. This will help us better address the overtourism problem and prevent any potential environmental damage it may cause. Our goal is to develop a more precise and effective solution for sustainable tourism management.

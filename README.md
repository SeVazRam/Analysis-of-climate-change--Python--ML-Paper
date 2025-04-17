# Analysis of Climate Change Based on Machine Learning and Endoreversible Model

## Description
This project analyzes global climate change through a hybrid approach that combines finite-time thermodynamic modeling with machine learning techniques. 
The focus is on forecasting terrestrial temperature trends by integrating physical models with data-driven predictions.

## Methodology
We model the Earth-Sun-Wind system as a thermodynamic heat engine based on a Gordon-Zarmi framework.  
The system's behavior is characterized by:
- Non-endoreversible parameters (R)
- Greenhouse effect parameter (γ)
- Albedo parameter (ρ)
- Solar radiation flux (q)

A set of thermodynamic equations is numerically solved using Wolfram Language to estimate the Earth's upper and lower atmospheric layer temperatures under maximum power conditions.  
Theoretical temperatures are then compared against observed data from historical records.

**Machine Learning Techniques Applied:**
- Linear Regression (LR)
- Ridge Regression (RR)
- Artificial Neural Networks (ANN)

These models are trained on historical land average temperature data to forecast future temperatures up to the year 2100.

## Data
Datasets used:
- `GlobalTemperaturesGZ.csv`: contains observed temperatures and model-generated temperature predictions using LR, RR, and ANN.
- `FinalGraphTemp.csv`: stores final processed data for plotting and evaluation.

The dataset from Berkeley Earth records monthly average land temperatures, which were aggregated to annual means for the analysis.  
A strong correlation (r = 0.89) was observed between the year and land average temperature from 1975 to 2015.

## How to Run
1. Clone this repository.
2. Navigate to the `/notebooks` folder.
3. Open and run:
   - `EDA_climate.ipynb` for exploratory data analysis.
   - `model_training.ipynb` for machine learning training and forecasting.
4. Review the comparison between theoretical and machine learning-based temperature projections.

> **Note:** All thermodynamic calculations are performed in Kelvin units.

## Results
- Thermodynamic models successfully predict terrestrial temperature evolution considering finite-time constraints.
- Machine learning models achieve high predictive accuracy when compared to experimental data.
- Forecasts show projected temperature trends up to 2100 under different modeling strategies.

## Paper Reference
For a detailed scientific discussion, please refer to our paper:  
**"Analysis of Climate Change Based on Machine Learning and Endoreversible Model"**  
(Available at: [Preprints Link](https://www.preprints.org/manuscript/202306.1197))

## Contact
Author: **Sebastián Vázquez Ramírez**  
Email: sebas.vaz.ra@gmail.com  
GitHub: [github.com/SeVazRam](https://github.com/SeVazRam)


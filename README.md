# anfis-wind-energy-prediction
# Wind Power Forecasting with ANFIS

This project analyzes wind SCADA data for one year and builds predictive models using Adaptive Neuro-Fuzzy Inference System (ANFIS) with various membership functions (MFs).

## 🎯 Objectives
- Analyze wind data trends and seasonal variations
- Predict wind power generation using ANFIS
- Compare different membership functions and evaluate model performance

## 📁 Dataset
- **Source:** Cleaned SCADA wind turbine data (`T1_cleaned_tableu.xlsx`)
- **Features:** (ALL values was normalized ,cause ANFIS works only values scaled [0,1].
  - Wind Speed (m/s)
  - Theoretical Power Curve (kWh)
  - LV ActivePower (kW)
  - Wind Direction (°)
  - Time-based features (month, season)

## ⚙️ Tools Used
- Python (for preprocessing and visualization)
- MATLAB (for ANFIS modeling)


## 📊 Model Configuration
| MF Type | MF Structure     | RMSE  |
|---------|------------------|-------|
| `trimf` | [4-2-2-2]         | 0.11  |
| `trapmf`| [4-2-2-2]         | 0.11  |
| `gbellmf`| [4-2-2-2]        | 0.11  |
| `gaussmf`| [2-2-2-3]        | 0.17  |

## 📈 Insights
- All MF types except `gaussmf` resulted in low RMSE (~0.11)
- Wind Speed and Theoretical Power strongly correlate with output
- The model performs well on normalized inputs and seasonal data

## 🧾 Files in this Repo
- `WindDATA.ipynb` – Python preprocessing & feature extraction
- `T1_cleaned_tableu.xlsx` – Cleaned dataset for modeling & visualization
- (Optional) MATLAB `.fis` or training script for reproducibility

# Traffic Volume Prediction (Interstate)

## Project Overview
This project aims to predict traffic volume on interstate highways based on date, time, weather conditions, and holidays. The goal is to help decision-makers optimize traffic management, logistics, and operational planning.

## Dataset
The dataset includes the following features:
- `traffic_volume`: Number of vehicles (target)
- `holiday`: Name of the holiday or None
- `temp`: Temperature in Celsius
- `rain_1h`: Rain amount in the last hour (mm)
- `snow_1h`: Snow amount in the last hour (mm)
- `clouds_all`: Cloud coverage (%)
- `weather_main`: General weather (Clear, Clouds, Rain, Snow, Mist)
- `date_time`: Date and time of the record

The dataset contains **historical traffic records** collected over multiple years.

## Data Preprocessing
- Converted `date_time` to datetime format
- Extracted `hour`, `day`, `month`, `weekday`, and `is_weekend` features
- Categorical variables (`holiday`, `weather_main`) were one-hot encoded

## Model
- **Random Forest Regressor** was used for prediction
- Pipeline included preprocessing (encoding + passthrough for numerical features)
- Train/Test split: 80% / 20%
- Evaluation metrics:
  - Mean Absolute Error (MAE)
  - R² Score

## Interactive Mini App
- Built using **ipywidgets** in Colab
- User inputs: DateTime, Temperature, Rain, Snow, Clouds, Holiday, Weather
- Output: Estimated traffic volume

## Feature Importance
The most important factors affecting traffic volume:
- Hour of the day
- Weather conditions
- Holiday
- Weekday/Weekend

Visualizations include:
- Hourly traffic patterns
- Holiday traffic impact
- Weekday vs weekend traffic

## How to Run
1. Open the notebook in Google Colab
2. Upload `traffic_volume_interstate.xlsx`
3. Run all cells sequentially
4. Use the mini app at the end to predict traffic volume

## Conclusion
This project provides a complete solution for traffic prediction with:
- Cleaned and feature-engineered data
- Accurate predictive model
- Interactive app for decision-makers
- Visual insights for operational planning



# HVAC Sensor Data Analysis

### Submitted by:

**Siva. R**
2nd Year, Department of Mechanical Engineering
ARM College of Engineering & Technology
Course: Data Analysis in Mechanical Engineering

---

## About This Project

This project is focused on analyzing HVAC (Heating, Ventilation, and Air Conditioning) sensor data. The goal is to understand how different environmental factors like temperature, humidity, airflow, CO₂ levels, and occupancy affect the energy usage of the HVAC system. By studying this data, we can find useful patterns and make suggestions that could help improve energy efficiency and maintain better air quality indoors.

This type of analysis can help in:

* Noticing how the HVAC system behaves over time.
* Finding situations where energy use is higher than normal.
* Supporting decisions in building management and maintenance.

---

## Dataset Summary

The dataset includes time-based records of various factors related to the indoor environment and HVAC system performance. Below is a brief explanation of each feature:

| Feature Name              | Description                                    |
| ------------------------- | ---------------------------------------------- |
| Date\_Logged              | The exact time and date when data was recorded |
| Temperature (C)           | Room temperature measured in Celsius           |
| Humidity (%)              | Percentage of indoor humidity                  |
| Air\_Flow (CFM)           | Airflow rate measured in cubic feet per minute |
| CO2\_Level (ppm)          | CO₂ concentration indoors (parts per million)  |
| Occupancy                 | Number of people in the room at that time      |
| Energy\_Consumption (kWh) | Energy used by the HVAC system (in kWh)        |

---

## How the Data Was Prepared

To prepare the data for analysis, the following steps were followed:

1. **Importing and Checking the Data**
   The dataset was loaded using pandas, and a quick look was taken to understand the type and structure of the data.

2. **Date and Time Formatting**
   The `Date_Logged` column was changed into datetime format to help with time-based analysis.

3. **Handling Missing Values**
   Some columns had missing values. These were filled using the average (mean) of those columns.

4. **Creating New Features**
   Additional useful features were created from the timestamp:

   * **Hour** – to see the time of day.
   * **DayOfWeek** – to know which day the data was recorded (e.g., Monday = 0).

---

## Exploring the Data

Various charts and graphs were used to better understand the data:

* **Time-Based Trends**

  * Energy use follows a daily pattern, going up during work hours.
  * CO₂ levels and temperature also change based on how many people are in the room.

* **Feature Relationships**

  * Energy usage is somewhat related to temperature and airflow.
  * CO₂ levels go up as more people are present.

* **Distributions and Outliers**

  * Some values, especially for energy and airflow, seem to be outside the usual range. Histograms and box plots were used to see this.

---

## What I Learned

* CO₂ levels increase when more people are in the room, which makes sense.
* The HVAC system increases airflow as occupancy rises — probably a smart system response.
* Energy use is highest during the day, mainly during office hours.
* Temperature and humidity don’t vary too much, which shows that the HVAC system is doing a good job maintaining stable conditions.

---

## What Can Be Done Next

* Use methods like the IQR technique to find and remove extreme values in the data.
* In the future, try building a prediction model to estimate energy usage or detect if the HVAC system is not working properly.

---

## Tools and Libraries Used

* **Python** – For writing the code and working with data

  * Libraries: **Pandas**, **NumPy**
* **Plotting** – To create visualizations

  * Libraries: **Matplotlib**, **Plotly**
* **Jupyter Notebook** – Used as the development environment


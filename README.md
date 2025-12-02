# 🌦️ Weather-Report-Project-1

A modern Weather & Air Quality Monitoring dashboard built in Power BI.  
This report combines live weather conditions, AQI metrics, and short‑term forecasts into a single interactive view for quick analysis.

---

## 🎯 Project Overview

This dashboard tracks real‑time weather for selected cities and presents temperature, humidity, visibility, wind, and pressure alongside air quality indicators such as PM10, PM2.5, O3, CO, NO2, and SO2.
It is designed as a portfolio‑ready analytics project that demonstrates working with APIs, Power Query (M), DAX, and a polished glassmorphism‑inspired UI in Power BI.

---

## ✨ Key Features

- 🌡️ Live temperature card with current condition (mist, sunny, cloudy, etc.) and city selector. 
- 📈 Multi‑day forecast line chart displaying expected temperature trends over time. 
- 💧 Dedicated tiles for humidity, wind speed, visibility, pressure, UV index, and precipitation.  
- 🟢 Air Quality Index section with gauge and cards showing PM10, PM2.5, O3, CO, NO2, SO2, plus qualitative status such as “Good / Moderate / Poor”.   
- 🌅 Sunrise and sunset panel for the selected city. 
- 🌧️ Chance‑of‑rain bar chart broken down by day of week for quick risk assessment.  
- 🎨 Dark theme with glassmorphism cards, custom icons, and conditional colors for an app‑like dashboard experience.

---

## 🛠 Tech Stack

- **Power BI Desktop** – data modeling, DAX measures, and report design. 
- **Power Query (M)** – connects to the weather API endpoint(s), transforms JSON responses, and shapes tables for current, forecast, and AQI data. 
- **Weather API provider** (for example, WeatherAPI or similar) – supplies live and forecast weather plus air quality metrics through HTTP endpoints. 
- **Power BI Service (optional)** – used to publish the report and schedule refresh so the dashboard always shows near real‑time data. 

---

## 📂 Data & Modeling

- Current weather and forecast are fetched from an HTTP API URL parameterized by city name or location.
- Power Query expands nested JSON fields (such as current, condition, air_quality, forecastday) and loads them into structured tables like `Current`, `DailyForecast`, and `Cities`.
- Relationships are built around a central `Cities` table so that slicers can filter all visuals by city with a single selection.

### 🔢 DAX Highlights

- Measures calculate rounded AQI values and classify them into text buckets (Good, Moderate, Unhealthy, etc.) that drive color formatting and labels.
- KPI measures for minimum, maximum, and average temperature, rain probability, and other metrics feed into cards, gauges, and charts. 

---

## 🚀 How to Run the Project

1. **Clone or download** this repository.  
2. Open the `*.pbix` file in **Power BI Desktop**.  
3. Go to **Transform Data → Manage Parameters** and update the parameter that stores your Weather API key and base URL (or edit the Web data source and paste your own API endpoint). 
4. Click **Refresh** to pull the latest weather and AQI data from the API. 
5. Explore the dashboard:
   - Use the city selector to switch between locations.  
   - Hover over the forecast chart for day‑wise details.  
   - Check the AQI and rain visuals to assess outdoor conditions. 

> ⚠️ You must obtain your own API key from the selected weather provider and follow their usage limits and terms of service. 

---

## 📸 Screenshots

- Main Weather & AQI overview page with real‑time metrics and forecast chart. 

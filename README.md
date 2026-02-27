# 🌫️ AQI Index Analysis: India Air Quality Dashboard

An interactive, data-driven Power BI dashboard built to explore and analyze Air Quality Index (AQI) trends across Indian states and cities — enabling real-time comparison of pollution levels, dominant pollutants, and seasonal patterns.

---

## 📌 Short Description / Purpose

The AQI Index Analysis Dashboard is a visually engaging Power BI report designed to help users monitor and compare air quality across Indian states and cities using dynamic filters, geo-mapping, and time-based trend analysis. The dashboard tracks key pollutants (PM2.5, PM10), AQI categories (Good to Hazardous), and city-level risk zones. It is intended for use by environmental analysts, public health researchers, policy makers, and data enthusiasts who want to understand India's air pollution landscape through data.

---

## 🛠️ Tech Stack

The dashboard was built using the following tools and technologies:

- 📊 **Power BI Desktop** – Main data visualization platform used for report creation and publishing.
- 📂 **Power Query** – Data transformation and cleaning layer for reshaping raw AQI data, handling nulls, and standardizing date formats.
- 🧠 **DAX (Data Analysis Expressions)** – Used for 15+ calculated measures including Avg AQI, Max AQI, AQI Category %, Pollutant Occurrence Frequency, Monthly Trend analysis, and dynamic KPI titles.
- 📅 **Calendar Table** – A custom date table built in DAX to enable time intelligence functions and month/year filtering.
- 🗺️ **Bing Maps Integration** – Used for geo-mapping AQI levels across Indian states.
- 📁 **File Format** – `.pbix` for development; `.png` for dashboard previews.

---

## 📂 Data Source

**Source:** Government air quality monitoring data (day-wise AQI readings across Indian cities)

The dataset (`day_wise_aqi_data`) contains day-level AQI readings for multiple Indian cities and states, including:

- `date` – Daily observation date
- `state` – Indian state name
- `area` / city – City or monitoring area
- `aqi_value` – Numeric AQI reading
- `air_quality_status` – Categorical status (Good, Moderate, Poor, Unhealthy, Very Unhealthy, Hazardous)
- `prominent_pollutants` – Primary pollutant recorded (PM2.5, PM10, PM2.5+PM10)
- `number_of_monitoring_stations` – Count of active stations in the area
- `unit` – AQI measurement unit

A supporting **Calendar Table** was created in DAX with `Date`, `Month`, and `Year` columns, linked to the main table via a many-to-one relationship on the date field.

---

## ✨ Features / Highlights

### 🔴 Business Problem

Air pollution is a critical public health challenge in India, with AQI levels frequently crossing hazardous thresholds in major cities. Yet, it's difficult for analysts, citizens, and policymakers to quickly identify:

- Which cities and states have the most dangerous AQI?
- What are the dominant pollutants driving poor air quality?
- How does air quality vary month-to-month or year-to-year?
- Where are monitoring gaps, and what regions are underserved?

Raw government data exists but is not easily navigable without a visual, interactive tool.

---

### 🎯 Goal of the Dashboard

To deliver an interactive visual tool that:

- Enables users to explore AQI trends across Indian states and cities with dynamic filtering.
- Identifies high-risk zones (AQI 200+) and tracks pollutant dominance over time.
- Supports decisions in public health awareness, environmental policy, and urban planning.
- Uncovers seasonal pollution spikes and regional patterns through time-intelligence analysis.

---

### 📊 Walkthrough of Key Visuals

**🔢 Key KPIs (Top Section)**
- **Max AQI:** 384 (filtered to Assam, 2025)
- **Primary Pollutant:** PM10
- **AQI Category:** Moderate
- Gauge chart displaying the current average AQI with a color-coded dial
- Dynamic titles update based on selected State filter

**🗺️ AQI by State (Map Visual)**
Geo-mapped bubble chart plotting AQI intensity across Indian states. Bubble size and color represent severity — from blue (good) to red (hazardous). Filters applied for Year, State, and City cascade across all visuals.

**📋 AQI Levels Reference Panel (Top Right)**
A color-coded legend showing AQI classification bands:
- 🟢 Good: 50–100
- 🟡 Moderate: 101–150
- 🟠 Poor: 151–200
- 🔴 Unhealthy: 210–250
- 🔴 Very Unhealthy: 251–300
- ⚫ Hazardous: >301

**📈 AQI Trend Over Time (Line Chart)**
Monthly AQI trend line with Year and Month slicers, showing seasonal patterns and pollution spikes. Useful for identifying winter months (Oct–Jan) as peak pollution periods.

**🏙️ AQI by City (Bar Chart)**
Horizontal bar chart ranking top cities by AQI value. Delhi tops the list at 208, followed by Hajipur (197), Gurugram (190), Panchkula (185), and Rohtak (178) — clearly flagging NCR as the highest-risk region.

**🍩 AQI Level Distribution (Donut Chart)**
Breakdown of records across AQI categories:
- Hazardous: 344 (44.1%)
- Good: 190 (24.36%)
- Moderate: 99 (12.69%)
- Unhealthy: 76 (9.74%)
- Very Unhealthy: 67 (8.59%)

**☁️ Pollutant Occurrence Frequency (Bar Chart)**
Tracks how often each pollutant appears as the primary driver:
- PM2.5: 101 occurrences
- PM10: 44 occurrences
- PM2.5 + PM10: 2 occurrences

**🎛️ Interactive Filters (Slicers)**
Three dropdown slicers allow users to drill into any combination of **Year**, **State**, and **City** — all visuals respond dynamically.

---

### 💡 Business Impact & Insights

- **Public Health Alerts:** Quickly identify cities where AQI regularly exceeds 200 (Unhealthy range) — Delhi, Hajipur, Gurugram — enabling targeted public advisories.
- **Pollutant Policy Focus:** PM2.5 dominates as the primary pollutant (101 vs 44 for PM10), suggesting vehicular and industrial emissions as the priority intervention area.
- **Seasonal Patterns:** The monthly trend line reveals winter pollution spikes, supporting evidence-based seasonal restrictions (e.g., stubble burning bans, odd-even traffic rules).
- **Regional Benchmarking:** State-level geo-map enables governments and NGOs to benchmark regions and allocate monitoring resources more effectively.
- **Data-Driven Awareness:** The dashboard can be embedded in public portals or used in presentations to drive citizen awareness about local air quality.

---

## 📸 Dashboard Preview

![AQI Index Analysis Dashboard](https://raw.githubusercontent.com/akavision/AQI-Index-Analysis/main/Snapshot%20of%20the%20Dashboard.png)

---

## 🚀 How to Use

1. Download and open `AQI_Analysis.pbix` in **Power BI Desktop**.
2. Use the **Year**, **State**, and **City** slicers at the top to filter data.
3. Hover over map bubbles to see state-level AQI details.
4. Use the **Month slicer** in the Trend section to explore monthly patterns.
5. Cross-filter by clicking any chart element to explore related visuals dynamically.

---

*Built by Akhilesh Madwalkar | Power BI | DAX | Data Analytics*

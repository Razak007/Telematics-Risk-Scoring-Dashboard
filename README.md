# 🚗 Telematics Risk Scoring Dashboard

A full data analytics project combining **Python** for data cleaning and preprocessing with **Power BI** for building a dynamic, multi-page dashboard. The dashboard helps analyze driving behavior, detect anomalies, and evaluate risk scores from vehicle telematics data.

---

## 📁 Project Structure

📦Telematics-Risk-Scoring-Dashboard
├── 📊 Telematics-Risk-Scoring-Dashboard.pbix
├── 📓 data_cleaning.ipynb
├── 📓 Devices_analysis.ipynb
├── 📁 data/
│ └── telemetry.csv (sample data)
├── 📷 assets/
│ └── dashboard-preview.png
└── README.md


---

## 📊 Dashboard Pages Overview

### 1. **Executive Overview**
- Key metrics: Risk Score, Brakes/100KM, Idle Time, Accelerations, Distance.
- Filters by `DeviceNumber`.
- Clean KPI layout for decision-makers.

### 2. **Device Risk Band Summary**
- Stacked bar chart by `RiskBand`.
- Color-coded by Low (Blue), Medium (Orange), High (Red).
- Data labels + conditional formatting applied.

### 3. **Telematics Behavior Explorer**
- GPS route visualized using `Latitude` & `Longitude`.
- Matrix for Speed, Engine, IdleFlags, TimeUTC.
- Conditional formatting:  
  - 🔴 Red for Harsh Braking  
  - 🟠 Orange for Harsh Acceleration

### 4. **Fraud / Anomaly Detection**
- Table highlighting suspicious cases:
  - Speed > 0 but Engine = 0.
  - Fuel drop with zero distance traveled.
- Flags: `FraudFlag_SpeedEngine`, `FuelDropNoDistance`.

### 5. **Documentation & Glossary**
- Explains dataset, logic, use cases.
- Includes link to creator’s GitHub/LinkedIn.

---

## 🔍 Data Summary

- **Total Devices**: 10
- **Data Points**: ~10,000+
- **Columns**: GPS, Speed, Engine RPM, Braking, Idle Time, Fuel Level, etc.

---

## 🧪 Python Processing

### 🔧 `data_cleaning.ipynb`
- Removed nulls
- Normalized Fuel, Speed, and Distance
- Feature engineered `BrakesPer100KM`, `IdlePer100KM`, etc.

### 📈 `Devices_analysis.ipynb`
- Aggregated risk score logic
- Outlier detection
- Device-level grouping

---

## 🧠 Risk Score Logic


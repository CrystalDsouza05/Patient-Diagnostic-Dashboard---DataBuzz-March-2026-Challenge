# 🏥 Patient Diagnostic Dashboard (Power BI)

![Power BI](https://img.shields.io/badge/Tool-Power%20BI-yellow)
![Analytics](https://img.shields.io/badge/Focus-Data%20Analytics-blue)
![Status](https://img.shields.io/badge/Project-Dashboard-purple)

## 📌 Project Overview

This project presents a **Patient Diagnostic Dashboard** designed to help healthcare professionals analyze patient health conditions, identify risks, and monitor trends over time.

The dashboard integrates:
- Patient symptoms  
- Diagnostic test results  
- Risk levels  
- Medication insights  
- Visit patterns  

It enables **data-driven clinical insights** through an interactive and structured Power BI report.

> ⚠ Disclaimer: This dataset is generated using AI and demographic data; the results may not be fully accurate.


## 🎨 Patient Diagnostic Dashboard

![Dashboard 2](https://github.com/user-attachments/assets/4492bbbd-d4f8-4196-a98f-4a044308f257)

Dashboard PDF in the files section

## 🎯 Objectives

The dashboard helps in:

- Identifying fever and illness patterns  
- Evaluating patient risk levels  
- Monitoring chronic indicators (Diabetes, BP, Asthma proxy)  
- Comparing current vs previous patient reports  
- Tracking patient visit trends  
- Understanding repeat patient behavior  
- Analyzing medication usage  

## 🧠 Data Modeling Approach

The dataset follows a **star schema** with clear relationships:

| Table | Role |
|------|------|
| Patient_Symptoms | Fact table (visit-level data) |
| Blood_Test_Results | Diagnostic details (linked via Visit_ID) |
| Fever_Type_Profile | Dimension (fever classification) |
| Medication | Linked via Fever_Type |
| Date_Table | Time intelligence |
| Patient | Unique patient-level table |

### Key Design Decisions:
- Visit-level analysis used to avoid double counting  
- USERELATIONSHIP used for Test_Date vs Visit_Date  
- Fever_Type_Profile acts as a bridge between fact and medication  


# 📊 DASHBOARD STRUCTURE


## 📘 PAGE 1: Patient Overview

### 🧭 Navigation Panel
A navigation pane on the left allows seamless switching between:
- Medical Overview  
- Patient Medical Report  

---

### 🎛 Slicers & Field Parameters

Slicers:
- Year (2024, 2025, 2026)

Field Parameters (Dynamic Analysis):
- Fever Type  
- Age Group  
- Risk Level  

These allow users to dynamically control and analyze visuals.

---

### 📊 Key KPIs

| KPI | Value | Description |
|-----|------|------------|
| Total Patients | 6,678 | Unique patients in dataset |
| High Risk % | 57.68% | % of patients categorized as high risk |
| Diabetes Indicator | 16,089 | Patients with glucose ≥ 140 |
| Asthma Indicator | 10,144 | Proxy using cough symptoms |
| Patients on Medication | 5,577 | Patients requiring treatment |

---

### ✨ Visuals

📉 Line Chart
**Title:** Visits by Patients (Trend)

- Displays monthly patient visits from Jan 2024 to Jan 2026  
- Range: ~695–746 visits per month  
- Helps identify seasonality and demand patterns  

---

🗺 Map Visualization
**Title:** Visits by Location

Shows geographic distribution of patient visits across:
- Hyderabad  
- Visakhapatnam  
- Vijayawada  
- Guntur  
- Tirupati  

---

📊 Bar Charts (Dynamic Section)

**Purpose:** Comparative analysis using field parameters  

| Metric | Dimensions |
|------|-----------|
| Total Patients | Fever Type / Age Group / Risk Level |
| Total Visits | Fever Type / Age Group / Risk Level |

Key Feature:
- Controlled via field parameters  
- Allows switching dimensions dynamically  
- Provides flexible and context-driven insights  

---

### 🧾 Insight Summary

This page answers:

- What is the overall patient load?  
- Which risk categories dominate?  
- How are visits distributed across demographics?  
- Are there noticeable trends over time?  

---

## 📘 PAGE 2: Medical Overview

### 📌 Purpose
Provides **clinical and diagnostic insights** using blood test data and patient segmentation.


### 📊 KPIs

| KPI | Value | Description |
|-----|------|------------|
| Total Patients for Tests | 6,678 | Patients with diagnostic records |
| Total Tests | 20,000 | Total tests conducted |
| Avg Hemoglobin | 13.01 | Blood health indicator |
| Avg Platelets | 2.52 | Critical for dengue/malaria |
| Avg WBC | 8,279 | Infection indicator |
| Avg CRP | 20.58 | Inflammation marker |

---

### 📊 Visuals

1️⃣ Stacked Bar Chart
**Title:** Category & Gender Distribution

- Displays patient distribution by category and gender  
- Toggle options:
  - Total Visits  
  - Total Patients  

**Categories:**
- Delayed  
- First Visit  
- Moderate  
- Regular  

2️⃣ Line Chart
**Title:** Hemoglobin & Platelets Trend

- Monthly trends (2024–2026)  
- Dual-line comparison  
- Helps identify deterioration/improvement  

3️⃣ Bar Chart
**Title:** Total Tests by Month

- Monthly diagnostic volume  
- Identifies testing spikes  

4️⃣ Donut Chart
**Title:** Patient Severity Distribution

- Controlled via field parameter  
- Can display:
  - Platelet Severity  
  - WBC Severity  
  - Diabetes  

**Categories:**
- Low  
- Normal  
- Severe  

5️⃣ Patient Data Table

| Column | Description |
|-------|------------|
| Patient_ID | Unique identifier |
| Fever_Type | Diagnosis |
| Medication Name | Prescribed medication |
| Risk_Level | Patient risk category |
| BP S/D | Blood pressure |

6️⃣ Test Summary Table

| Column | Description |
|-------|------------|
| Patient_ID | Unique identifier |
| Total Tests | Number of tests |
| Avg Platelets | Blood indicator |
| Avg Temperature | Fever severity |
| Avg Hemoglobin | Health indicator |

---

### 🎛 Slicer

- Year slicer applied globally  
- Ensures consistent filtering across all visuals  

---

### 🧾 Insight Summary

This page answers:

- What do diagnostic reports indicate?  
- Are blood indicators improving or worsening?  
- Which patients are at higher clinical risk?  

---

## 📘 PAGE 3: Patient Medical Report

### 📌 Purpose

Provides a **detailed patient-level view** for individual analysis.

---

### 📊 KPIs

| KPI | Value |
|-----|------|
| Total Tests | 10 |
| Avg Hemoglobin | 13.50 |
| Avg Platelets | 2.74 |
| Avg WBC | 8,758 |
| Avg CRP | 22.00 |
| Avg Temperature | 39.05 |
| Asthma Indicator | 6 |
| Diabetes Indicator | 6 |

---

### 📊 Detailed Sections

🧍 Patient Demographics

- Age Group  
- Gender  
- Visit Dates  
- Total Visits  

🤒 Symptom Tracking

- Headache  
- Chills  
- Cold  
- Cough  
- Diarrhea  
- Rash  
- Abdominal Pain  
- Joint Pain  

✔ Present  
❌ Absent  

🍬 Diabetes Category

| Range | Category |
|------|--------|
| <140 | Normal |
| 140–199 | Prediabetes |


### ⚡ Fatigue Levels

| Level | Color |
|------|------|
| High | Red |
| Medium | Yellow |
| Low | Blue |

🏥 Admission Status

- Indicates whether hospitalization is required  

---

🎛 Slicer

- Year filter applied across the page  

---

🧾 Insight Summary

This page answers:

- What is the condition of a specific patient?  
- Are symptoms worsening or improving?  
- What do diagnostic trends indicate?  

---

🚀 Key Highlights

- Avoids double counting using visit-level analysis  
- Combines clinical + behavioral insights  
- Uses advanced DAX (USERELATIONSHIP, comparison logic)  
- Interactive and dynamic filtering  

---

## 🛠 Tools Used

- Power BI
- Excel 
- DAX  
- Data Modeling
- Figma & Power Point
- Measure Killer








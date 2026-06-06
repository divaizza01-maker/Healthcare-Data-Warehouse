
# Healthcare Data Warehouse & OLAP Analysis

## 📊 Project Overview

Proyek ini merupakan implementasi **Data Warehouse berbasis OLAP** untuk analisis data kesehatan pasien dengan fokus pada:

- Faktor risiko penyakit medis
- Analisis demografi pasien
- Analisis billing rumah sakit
- Analisis lama perawatan (Length of Stay)
- Visualisasi multidimensional menggunakan Atoti Dashboard

Sistem dibangun menggunakan pipeline lengkap:

> **ETL → PostgreSQL Data Warehouse → Star Schema → Optimization → OLAP Cube (Atoti) → Dashboard**

---

## 🎯 Objectives

Proyek ini bertujuan untuk:

- Mengintegrasikan data kesehatan menjadi Data Warehouse terstruktur
- Membangun Star Schema untuk analisis multidimensional
- Mengoptimalkan query menggunakan Index & Materialized View
- Membuat OLAP Cube menggunakan Atoti
- Menyediakan dashboard interaktif untuk analisis data

---

## 📂 Dataset

Dataset yang digunakan:

- Healthcare Dataset (CSV)
- Berisi data pasien, rumah sakit, kondisi medis, dan administrasi

### Kolom utama:
- Name
- Age
- Gender
- Blood Type
- Medical Condition
- Date of Admission
- Discharge Date
- Hospital
- Insurance Provider
- Billing Amount
- Length of Stay
- Admission Type
- Medication
- Test Results

---

## 🏗️ Architecture

```

CSV Dataset
↓
ETL Process (Python + Pandas)
↓
Data Cleaning & Transformation
↓
PostgreSQL Data Warehouse
↓
Star Schema Design
↓
Indexing + Materialized View
↓
OLAP Cube (Atoti)
↓
Interactive Dashboard

```

---

## 🧱 Data Warehouse Design

### Fact Table
- fact_healthcare
  - Billing Amount
  - Length of Stay
  - jumlah_pasien

### Dimension Tables
- dim_patient (Gender, Age, Blood Type)
- dim_medical (Medical Condition, Medication, Test Result)
- dim_hospital (Hospital, Doctor, Insurance Provider)
- dim_admission (Admission Type, Room Number)
- dim_admission_time (Date of Admission breakdown)
- dim_discharge_time (Discharge Date breakdown)

---

## ⚙️ Technologies Used

- Python (Pandas, NumPy)
- PostgreSQL
- SQLAlchemy
- Atoti OLAP Engine
- Matplotlib / Pandas (analysis)
- Jupyter Notebook

---

## 🔄 ETL Pipeline

### Extract
- Load dataset dari CSV

### Transform
- Cleaning data
- Handling missing values
- Feature engineering (Age Group, Time Dimension)
- Category encoding

### Load
- Insert data ke PostgreSQL Data Warehouse
- Build Star Schema

---

## 🚀 PostgreSQL Optimization

Implemented optimizations:

- Indexing pada foreign key
- Materialized View untuk summary query
- Benchmark query performance
- Query execution comparison

---

## 📊 OLAP Cube (Atoti)

Fitur OLAP:

- Hierarchies:
  - Time (Year, Month, Day)
  - Patient (Gender, Age Group)
  - Medical Condition
  - Hospital
  - Admission Type

- Measures:
  - Total Patients
  - Average Billing
  - Average Length of Stay

---

## 📈 Dashboard

Atoti Dashboard menyediakan visualisasi:

- Distribusi pasien berdasarkan usia & gender
- Analisis penyakit berdasarkan kondisi medis
- Analisis billing rumah sakit
- Trend data berdasarkan waktu
- Multidimensional OLAP exploration

---

## 📁 Project Structure

```

Healthcare-Data-Warehouse/
│
├── data/
├── notebooks/
├── scripts/
├── dim_patient.csv
├── dim_medical.csv
├── dim_hospital.csv
├── dim_time.csv
├── fact_healthcare.csv
├── etl_pipeline.ipynb
├── olap_atoti.py
├── README.md

```

---

## 👨‍💻 Team

- Amelia Salsabila Ar Rofik (24031554128)
- Diva Izza Mansyanthika (24031554217)
- Savitri Rahmaning Lukito (2403155219)

---

## 🔗 Repository

GitHub:
```

[https://github.com/divaizza01-maker/Healthcare-Data-Warehouse](https://github.com/divaizza01-maker/Healthcare-Data-Warehouse)

```

---

## 📌 Conclusion

Project ini berhasil membangun sistem Data Warehouse lengkap berbasis OLAP yang mampu:

- Mengintegrasikan data kesehatan
- Menyediakan analisis multidimensional
- Mengoptimalkan query analytics
- Menyediakan dashboard interaktif menggunakan Atoti

---

## ⭐ Future Work

- Integrasi Machine Learning untuk prediksi penyakit
- Streaming real-time data ingestion
- Dashboard berbasis web (Streamlit / Power BI)
```

---

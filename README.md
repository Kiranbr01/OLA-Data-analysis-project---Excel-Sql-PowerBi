# OLA-Data-analysis-project---Excel-Sql-PowerBi
# 🚖 OLA Mobility Data Analytics Project  
### Power BI • SQL • Excel • Ride Insights • Cancellations • Revenue • Ratings • KPI Dashboard

This project is an end-to-end **Business Intelligence & Data Analytics case study** based on OLA's ride-hailing operations.  
It showcases complete BI skills: **Excel cleaning → SQL analysis → Power BI dashboarding → Insight generation**.

## Dataset Used --
- <a href="

---

## 📌 Project Summary
This project analyzes OLA’s daily ride data to extract business insights related to:

- Ride demand & hourly trends  
- Revenue & fare patterns  
- Customer vs driver cancellations  
- Vehicle category performance  
- Customer & driver satisfaction scores  
- Payment behavior (UPI, Cash, Wallet, Card)  
- Operational KPIs such as CTAT, VTAT, ride distance, and fare efficiency  

The goal is to understand operational inefficiencies, customer behavior, and ride performance trends.

---

## 🛠 Tools Used
| Tool | Purpose |
|------|---------|
| **Excel** | Data Cleaning, Formatting, Feature Engineering |
| **SQL (MySQL Workbench)** | KPI Calculation, Aggregations, Ride Insights |
| **Power BI** | Dashboard Building, DAX KPIs, Interactive Visualizations |
| **PDF Report** | Business Summary and Findings |

---

## 📊 Power BI Dashboard (Screenshots)

> *(Upload screenshots to `powerbi/screenshots` for these links to work)*

### 🔹 Overview Dashboard  
![Overview](powerbi/screenshots/overview.png)

### 🔹 Vehicle Type Performance  
![Vehicle Types](powerbi/screenshots/vehicle_types.png)

### 🔹 Revenue Dashboard  
![Revenue](powerbi/screenshots/revenue.png)

### 🔹 Cancellation Analysis  
![Cancellations](powerbi/screenshots/cancellations.png)

### 🔹 Rating Insights  
![Ratings](powerbi/screenshots/ratings.png)

---

## ⭐ Power BI KPIs Included

The Power BI dashboard includes the following interactive KPIs:

- **Total Rides**  
- **Completed Rides**  
- **Cancelled Rides**  
- **Cancellation Rate**  
- **Average Customer Rating**  
- **Average Driver Rating**  
- **Total Revenue**  
- **Average Fare per KM**  
- **Vehicle-wise Ride Share**  
- **Top Peak Hours**  
- **City Hotspots**  
- **Payment Method Share**  

All KPIs were built using:
- DAX Measures  
- Power Query Transformations  
- Custom Data Modeling  
- Drill-through Pages  
- Slicers (Vehicle Type, Payment Type, Time Filter)

---

## 🧠 Key Insights

### 🚗 Ride Demand Trends  
- Morning (8–11 AM) and Evening (5–9 PM) are peak ride hours  
- Weekend rides increase by **30–40%**

---

### ❌ Cancellation Insights  
- Driver cancellations are **higher** than customer cancellations  
- Autos & Bikes have the highest cancellation percentage  
- Peak hour cancellations are mainly due to long pickup times  

---

### 💸 Revenue Insights  
- **Prime Sedan** has the highest per-ride revenue  
- UPI dominates with **55%+** of payments  
- Less revenue after 11 PM due to low demand  

---

### ⭐ Ratings Analysis  
- Avg Customer Rating → **4.2**  
- Avg Driver Rating → **4.4**  
- SUVs receive the highest satisfaction rating  
- Short-distance rides slightly reduce customer rating (traffic frustration)

---

## 🗂 Dataset Fields
The dataset includes:

- Booking Date & Time  
- Pickup Location  
- Drop Location  
- Vehicle Type  
- Booking Status  
- Cancelled By (Driver/Customer)  
- Ride Distance (KM)  
- Fare Amount  
- Payment Method  
- Customer Rating  
- Driver Rating  
- VTAT (Vehicle Time to Arrive)  
- CTAT (Customer Time to Arrive)  

---

## 🧮 SQL Query Examples

### 1️⃣ Cancellation Breakdown  
```sql
SELECT cancelled_by, COUNT(*) AS total_cancellations
FROM ola_bookings
WHERE booking_status = 'Cancelled'
GROUP BY cancelled_by;

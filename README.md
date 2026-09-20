# IBM-HR-Attrition-Analysis-Dashboard-Power-BI

A clean, end-to-end Power BI dashboard designed to transform raw HR employee data into intuitive operational insights. This project focuses on production-ready business intelligence development principles: intuitive UI/UX design, high data scannability, and clear data storytelling.

Instead of overcomplicating the analytics with unnecessary code, this solution prioritizes a highly organized multi-page interface that allows HR managers and site leaders to navigate from high-level headcount trends down to granular root-cause retention risk audits effortlessly.

---

## 📸 Interface Analytics Views

### 1. Executive Overview
Utilizes the standardized core dashboard layout to track macro-level workforce health, active headcount, overall turnover rate, and core demographic distributions across departments and job roles.
* **Visual Asset:** `overview ibm rh.png`

### 2. Detailed Breakdown
Shares the identical structural design framework as the Executive Overview to maintain visual consistency, but operates as a deep-dive retention dashboard configured to analyze psychometric satisfaction scores, career stagnation trends, overtime impact multipliers, and salary band hotspots.
* **Visual Asset:** `Detailed Breakdown IBM HR .png`

---

## 💡 Key Business Insights

* **The Overtime Multiplier:** Overtime is the single largest driver of turnover. Employees working overtime have a **30.53% attrition rate** compared to just **10.44%** for those who do not. 
* **Early-Career & Compensation Flight Risk:** The highest concentration of departures occurs in the **Under 3K** monthly salary band (**28.61% attrition**), heavily overlapping with the **<25 age group** (**39.18% attrition**).
* **Career Stagnation Spikes:** Retention drops sharply for employees who reach **3 to 5 years without a promotion**, indicating a critical window where intervention and career mobility planning are required.

---

## 📐 Key Metrics & DAX Logic Explained

To move beyond basic headcount counting, several custom metrics were developed using DAX to surface actionable risk factors:

* **OverTime Impact Factor (2.93x):** A calculated ratio comparing the attrition rate of overtime workers against non-overtime workers. A resulting factor of 2.93 means employees logging overtime are nearly **3 times more likely to leave** the company.
* **High Risk Employee (97 Active):** A targeted retention flag identifying *currently active* employees who score poorly (2 or lower out of 4) in both **Job Satisfaction** and **Environment Satisfaction**. This serves as a targeted "stay interview" list for HR.
* **Avg JobSat % (Rated 3/4):** Rather than showing a vague average score (e.g., 2.7/4), this metric calculates the exact percentage of the workforce that rates their job satisfaction as High or Very High (currently at **61.29%**).

---

## 🛠️ Core Implementation & Design Details

* **App-Style Interface Layout:** Engineered a top navigation tab system utilizing reactive button states (Overview vs. Detailed Breakdown) to transform a standard report file into a modern web-app experience.
* **Inline KPI Conditional Alerts:** Configured structural formatting rules and custom DAX measures directly inside card containers to highlight immediate retention risks.
* **Chronological & Ordinal Sorting Logic:** Implemented background logical sorting indices to guarantee that ordinal categories such as Salary Bands, Satisfaction levels, and Age Groups align logically rather than alphabetically.
* **Production-Ready Theme:** Applied a cohesive IBM Corporate Blue and high-contrast alert color palette optimized for high visual scannability and quick executive reporting.

---

## 📊 Dataset Specifications
* **Source:** IBM HR Analytics Employee Attrition & Performance dataset (`WA_Fn-UseC_-HR-Employee-Attrition.csv`).
* **Volume:** 1,470 unique employee records indexed across 35 operational and demographic metrics.
* **Data Prep:** Cleaned data types, created calculated DAX measures for Attrition Rate %, Active Headcount, OverTime Impact Factor, and isolated custom Salary Band groupings.

---

## ⚙️ How to Explore the Project
1. Clone this repository to your local machine:
   ```bash
   git clone [https://github.com/your-username/IBM-HR-Attrition-Analysis-Dashboard-Power-BI.git](https://github.com/your-username/IBM-HR-Attrition-Analysis-Dashboard-Power-BI.git)

# student-competency-performance-analytics
# 📊 Student Performance & Competency Analytics Dashboard (Power BI)

An advanced Business Intelligence and Data Engineering project designed to transform traditional academic reporting into a **strategic, collaborative, and proactive educational ecosystem**. 

This repository showcases the technical pipeline and dynamic data modeling required to build an actionable decision-making tool for educational institutions, academic leaders, and student counselors.

---

## 🎯 Educational Value & Strategic Objectives
Modern education is shifting from static grade-tracking to a holistic approach focused on **student potential and proactive support**. This dashboard serves that vision by:
- **Nurturing Competencies:** Integrates academic grades, behavior metrics, and attendance into a single, weighted **Student Competency Score**. This allows educators to discover and elevate student strengths rather than just focusing on academic deficits.
- **Proactive Counseling (Early Warning System):** Correlates attendance risk levels with performance gaps. This builds a collaborative bridge for student counselors to execute early interventions for high-risk students.
- **Root Cause Analysis:** Empowers decision-makers to dig deeper into performance drops using **Decomposition Trees**—drilling down smoothly from Gender, Academic Branch, and Grade Level, directly to individual student cases.

---

## 🛠️ Tech Stack & Engineering Highlights
- **BI Tool:** Microsoft Power BI Desktop
- **Data Engineering (ETL):** Power Query (used for data profiling, cleansing, and cross-table normalization).
- **Analytical Calculations:** Advanced DAX (Data Analysis Expressions) for creating optimized, dynamic metrics and clean numerical outputs.
- **UX/UI Best Practices:** Applied a modern Dark Theme architecture (Fluent 2 standards) to ensure high readability and reduce visual fatigue for long-term daily enterprise use.

---

## 📐 Data Modeling & Core DAX Metrics
The project establishes a highly dynamic data schema linking student demographic tables with continuous performance records across Grade Levels (1st, 2nd, and 3rd Secondary).

A key implementation is the calculated **Student Competency Metric**, weighted as follows:
- **Academic Performance:** 60%
- **Attendance Rate:** 30%
- **Behavioral Track:** 10%

```dax
مؤشر جدارة الطلاب = 
VAR AverageGrade = CALCULATE(AVERAGE('الأداء الأكاديمي والدرجات'[الدرجة (من 100)]))
VAR AttendanceScore = 'بيانات الطلاب الشخصية'[% معدل الحضور العام]
VAR BehaviorScore = CALCULATE(AVERAGE('الأداء الأكاديمي والدرجات'[نقاط السلوك])) * 10

RETURN 
ROUND(
    (AverageGrade * 0.60) + (AttendanceScore * 0.30) + (BehaviorScore * 0.10),
    2
)
```

---

## 🖼️ Dashboard Preview & Architecture
Below is a comprehensive visual snapshot of the interactive application interface:

![Dashboard Preview](student-competency-performance-analytics.jpeg)


---

## 📁 Repository Structure
- `Student_Analytics.pbix` - The primary production-ready Power BI application file.
- `README.md` - Documentation and structural business breakdown.

---
*Developed by a Data Analytics Engineer passionate about transforming raw educational data into high-value strategic execution. Feel free to explore the repository, open issues, or connect with me via LinkedIn!*

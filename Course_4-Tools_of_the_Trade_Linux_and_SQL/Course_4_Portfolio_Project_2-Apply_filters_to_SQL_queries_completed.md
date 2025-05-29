# 🛡️ Course 4 Portfolio Project 2: Apply Filters to SQL Queries

## 📘 Introduction

In this project, I acted as a security analyst investigating potential threats and anomalies in SQL logs. Using a variety of filtering techniques (`AND`, `OR`, `NOT`, and `LIKE`), I performed a deep analysis of login attempts and employee records. This helped identify security patterns and suspicious activities.

---

## 🔍 Query Results & Explanations

### 1. Retrieve After-Hours Failed Login Attempts

![Query Screenshot: After-Hours Failed Logins](Course_4-Tools_of_the_Trade_Linux_and_SQL\Portfolio_project_2_screenshots\1.png)
**Explanation:** Retrieves logins where `success = 0` and `login_time > '18:00'`, highlighting unusual failed attempts outside business hours.

---

### 2. Retrieve Login Attempts on Specific Dates

![Query Screenshot: Specific Dates](Course_4-Tools_of_the_Trade_Linux_and_SQL\Portfolio_project_2_screenshots\2.png)  
**Explanation:** Filters logins on May 8 and 9, 2022 using the `OR` operator—useful for event-driven investigations.

---

### 3. Retrieve Login Attempts Outside of Mexico

![Query Screenshot: Not Mexico](Course_4-Tools_of_the_Trade_Linux_and_SQL\Portfolio_project_2_screenshots\3.png)
**Explanation:** Uses `NOT LIKE '%MEX%'` to exclude logins originating from "MEX", helping spotlight foreign access.

---

### 4. Retrieve Employees in Marketing in East Buildings

![Query Screenshot: Marketing East](Course_4-Tools_of_the_Trade_Linux_and_SQL\Portfolio_project_2_screenshots\4.png)
**Explanation:** Filters employees in the Marketing department working in offices like “East-170” using `LIKE 'East%'`.

---

### 5. Retrieve Employees in Finance or Sales

![Query Screenshot: Finance or Sales](Course_4-Tools_of_the_Trade_Linux_and_SQL\Portfolio_project_2_screenshots\5.png)
**Explanation:** Uses `OR` logic to get employees from both departments—helpful for departmental audits.

---

### 6. Retrieve All Employees Not in IT

![Query Screenshot: Not IT](Course_4-Tools_of_the_Trade_Linux_and_SQL\Portfolio_project_2_screenshots\1.png)
**Explanation:** Uses `NOT` to filter out employees in IT, useful for reviewing users pending system updates.

---

## 🧠 Summary

By applying SQL filters effectively, I was able to:

- Pinpoint login anomalies and potential breaches
- Narrow data to relevant departments and geographic regions
- Build queries to enhance security visibility and mitigate threats

---

## 📌 Tools Used

- SQL
- Logical and pattern-matching operators (`AND`, `OR`, `NOT`, `LIKE`)
- Data visualization via query screenshots

---

## ✅ Key Takeaways

- SQL filtering helps isolate abnormal activity patterns
- Query logic is essential in investigations
- Clear documentation supports reproducibility and collaboration

---

📄 **[View Full Report on Google Docs](https://docs.google.com/document/d/19Y4DLTpkRkJYTS0kbEXYXVIxWnRjtFFgU7K1U2bAQyo/edit?usp=sharing)**

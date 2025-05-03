

# HR Analytics Dashboard – Power BI

## 📊 Project Overview
This Power BI dashboard provides comprehensive insights into HR data, focusing on **employee demographics**, **turnover analysis**, and **gender distribution**. Built as a portfolio project to showcase my skills as a **Junior Power BI Developer** and **Data Analyst**, it uses real-world KPIs and visual storytelling techniques to support data-driven decision-making.

---

## ❓ Analytics Questions Answered

- 🔹 How many employees are currently in the company?
- 🔹 What is the gender distribution of the workforce?
- 🔹 What is the percentage of male vs female employees?
- 🔹 How many employees have left the organization (turnover)?
- 🔹 What is the employee turnover rate?
- 🔹 What is the age of each employee?
- 🔹 What is the average age of employees?
- 🔹 Are there gender-based trends in turnover?

---

## 🧠 Key Business Insights

- ✅ The company has a balanced gender distribution with a slight skew toward [female/male].
- ✅ The turnover rate is approximately **X%**, indicating [healthy turnover / retention issues].
- ✅ Most terminated employees fall within the **[X–Y]** age group.
- ✅ Gender distribution in turnover is [balanced / skewed].
- ✅ Age diversity is evident with an average employee age of **Z years**.

---

## 🧮 DAX Formulas Used

### 🔹 Turnover Label (Column):
```dax
Turn over label = NOT(ISBLANK('HR(Fact)'[Termination Date]))
````

### 🔹 Age Calculation (Column):

```dax
Age = DATEDIFF('HR(Fact)'[Birth Date], TODAY(), YEAR)
```

### 🔹 Total Employees (Measure):

```dax
Total Employees = COUNTROWS('HR(Fact'))
```

### 🔹 Female Count (Measure):

```dax
Female Count = CALCULATE(COUNTROWS('HR(Fact')), 'HR(Fact)'[Gender] = "Female")
```

### 🔹 Male Count (Measure):

```dax
Male Count = CALCULATE(COUNTROWS('HR(Fact')), 'HR(Fact)'[Gender] = "Male")
```

### 🔹 Female % (KPI Measure):

```dax
Female Percentage = DIVIDE([Female Count], [Total Employees], 0)
```

### 🔹 Male % (KPI Measure):

```dax
Male Percentage = DIVIDE([Male Count], [Total Employees], 0)
```

### 🔹 Turnover Count (Measure):

```dax
Turnover Count = CALCULATE(COUNTROWS('HR(Fact')), NOT(ISBLANK('HR(Fact)'[Termination Date])))
```

### 🔹 Turnover Rate (% of all employees):

```dax
Turnover Rate = DIVIDE([Turnover Count], [Total Employees], 0)
```

---

## 📊 Visualizations & Charts

* ✅ KPI Cards: Total Employees, Male %, Female %, Turnover Rate
* ✅ Bar Chart: Gender Distribution
* ✅ Pie Chart: Gender Composition
* ✅ Table: Employee Age, Gender, Termination Status
* ✅ Column Chart: Turnover by Gender or Age Group

All visuals are **interactive** and designed using **Power BI best practices** for clean, readable layouts.

---

## 🔧 Technical Skills & Tools

* **Power BI Desktop**
* **DAX (Data Analysis Expressions)**
* **Data Modeling**
* **ETL / Data Cleaning**
* **KPI Reporting & Visualization**
* **Interactive Dashboards**
* **Insight Communication**

---

## 📁 Dataset

A simulated HR dataset containing:

* Employee Gender
* Birth Date
* Termination Date

> Used for educational and portfolio purposes only.

---

## 🧑‍💻 Author

Hasnaa Ahmed
Junior Data Analyst | Power BI Developer

📧 Email: \[[your.email@example.com](mailto:your.email@example.com)]
🔗 LinkedIn: \[Your LinkedIn Profile]
🌐 Portfolio: \[Your Portfolio Link]

---

## 📌 Keywords

`Power BI`, `HR Dashboard`, `DAX`, `Data Analysis`, `Turnover Rate`, `Gender Distribution`, `Interactive Dashboard`, `KPI Metrics`, `Workforce Analytics`, `Junior Data Analyst`, `Microsoft Power BI`, `Data Visualization`, `Business Intelligence`, `Storytelling with Data`, `Employee Insights`

```

---

This README will make your GitHub repo or project **shine in job applications or portfolios**!  
Would you like me to help you turn this into a downloadable PDF for a CV attachment or LinkedIn project?
```

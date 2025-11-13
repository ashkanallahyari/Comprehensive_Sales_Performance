# Power BI Sales & Customer Analytics Dashboard

## Project Overview

This Power BI project provides a **comprehensive analytical view of sales performance, customer behavior, and retention patterns** for a retail company.
The goal is to enable data-driven decisions by visualizing key performance indicators (KPIs) and uncovering actionable insights about customers, regions, and product performance.

The report follows a **progressive analytical structure** — from high-level business performance to deep behavioral analysis and root cause diagnostics.

---

## Data Model & Preparation

### Data Import

* **Dynamic Path Configuration:** A Power BI parameter `DataFolderPath` is created to dynamically control the base address of the datasets, ensuring easy migration and scalability.
* **Data Model Design:**

  * Dimensional tables (e.g., *DimCustomer, DimProduct, DimTerritory, DimDate*) are placed at the top of the model.
  * Fact tables (e.g., *SalesOrderHeader, SalesOrderDetail*) form the lower layer.
  * One-to-many relationships are used with referential integrity enforced.
  * Surrogate keys and lookup relationships are optimized for data consistency.

<img width="1450" height="690" alt="{A33C06C7-F847-46B2-A151-1B13B4D5FCD1}" src="https://github.com/user-attachments/assets/6b5fd757-07d2-4d93-a39b-40ee42fe40e1" />

---

## Dashboard Pages & Insights

### **Page 1 – Sales Performance Overview**

**Goal:** “How are we performing in orders, customers, and sales?”

**Key Business Questions**

* How much revenue have we generated (Total Sales)?
* Are we processing more orders or selling more individual units?
* What is the average order value (AOV)?
* Which product categories drive the most revenue?
* Which regions contribute most to total sales?
* How does performance compare year-over-year?
* What portion of sales occur online vs. offline?

**Highlights**

* KPIs: Total Sales, Orders, Units Sold, AOV
* Visuals:

  * Sales by Product Category
  * Top 10 Subcategories
  * Sales by Region
  * Sales Trend Over Time
* Purpose: Provide executives a one-glance overview of company performance and revenue drivers.
* 
<img width="1290" height="732" alt="{2A92EAC6-54F1-4CD9-93EB-551226F607D1}" src="https://github.com/user-attachments/assets/db0cefdf-7ba8-43f3-a359-a85ea29d29f2" />

---

### **Page 2 – Regional & Territory Performance**

**Goal:** “Where are we performing well geographically, and what regions need attention?”

**Key Business Questions**

* Which territories drive most of our sales?
* How does performance vary across continents (Europe, North America, Pacific)?
* Which regions have the most active customers?
* What products dominate each region?

**Highlights**

* Map visualization of sales by territory
* Regional KPIs: Orders, Active Customers, Units Sold
* Top Territories by Revenue
* Trend comparison across regions over time

<img width="1295" height="738" alt="{0D9DAFD7-6780-49E5-9955-F9045AFA32E4}" src="https://github.com/user-attachments/assets/9e61331e-9577-4b2e-885b-8f4988d9d801" />

---

### **Page 3 – Customer Persona & Behavior**

**Goal:** “Who are our customers and what are their purchasing behaviors?”

**Key Business Questions**

* What is the profile of a typical customer (demographics & lifestyle)?
* What is the average customer lifetime value (CLV)?
* How often do customers place orders?
* How do demographics correlate with spending or activity?

**Highlights**

* Persona-based visuals (Gender, Age, Education, Marital Status, Occupation)
* Financial segmentation (Income, Home Ownership, Number of Cars)
* Behavioral insights (Orders per Customer, Average Order Size)
* Dynamic filtering by Product, Category, or Region

<img width="1295" height="739" alt="{59D2615A-C098-494D-86DA-008C6BF981C3}" src="https://github.com/user-attachments/assets/c6a4e3f1-84a9-452a-8aaa-e033be302510" />

<img width="1294" height="738" alt="{79390F54-D695-4885-89D8-E081E0DC6C9A}" src="https://github.com/user-attachments/assets/e16568a1-694b-425a-a439-8bda3dd81245" />


---

### **Page 4 – Online Customer Behavior & Engagement**

**Goal:** “How efficiently are we converting online engagement into sales?”

**Key Business Questions**

* How many customers engage online vs. offline?
* What is our Cart-to-Sale conversion rate?
* Which devices, browsers, or OSs are most used by customers?
* How is online revenue trending?

**Highlights**

* KPIs: Online Orders, Online Sales, Conversion Ratios
* Trend analysis of online performance
* Technology segmentation (OS, Browser)
* Channel comparison (Online vs. Offline Sales)

<img width="1297" height="735" alt="{DE4EE8AB-D29D-4CCD-843B-7E15476CB230}" src="https://github.com/user-attachments/assets/cbb49e6f-e879-4067-ab42-870257680052" />


---

### **Page 5 – Cohort Analysis: Repeat Purchase Behavior**

**Goal:** “How do our customers behave after their first purchase?”

**Key Business Questions**

* What percentage of customers make a second, third, or fourth purchase?
* How long does it take for repeat orders?
* Which cohorts have the highest retention rates?
* How does retention differ across demographics or channels?

**Highlights**

* Cohort Retention Heatmap (Month 0–12)
* Customer lifecycle visualizations (1st–4th purchase timing)
* Retention trend line by cohort
* Contextual demographic and regional breakdowns

<img width="1295" height="737" alt="{78B38442-5F84-4AD2-98C0-1403FD44005D}" src="https://github.com/user-attachments/assets/992c4ec8-278a-48b4-bbab-982a13d8cede" />


---

### **Page 6 – Root Cause Analysis (Decomposition Tree)**

**Goal:** “What factors drive our sales performance?”

**Key Business Questions**

* Which product, demographic, or region combinations drive high or low sales?
* How do multiple attributes (Gender × Product × Income) interact in performance?
* Where are unexpected spikes or declines occurring?

**Highlights**

* Dynamic **Decomposition Tree**
* Drill-down capability by Product, Subcategory, Gender, Marital Status, Occupation, Income
* Data storytelling through multi-level contribution analysis

<img width="1299" height="731" alt="{A53DAE79-3627-4BCB-8D71-D27E4A3F0833}" src="https://github.com/user-attachments/assets/4a7a1e06-35b1-403b-89ed-05ed2da49f9a" />


---

## Key Learnings & Insights

* Clear structuring of pages from macro to micro (Sales → Region → Customer → Online → Retention → Root Cause)
* Effective balance between **business storytelling** and **technical DAX modeling**
* Dynamic, time-sensitive cohort analysis using DAX virtual tables
* Visual design consistency following professional BI principles (focus, hierarchy, alignment)

---

## Tools & Technologies

* **Power BI Desktop**
* **DAX**
* **Power Query (M Language)**
* **Data Modeling (Star Schema)**
* **GitHub for version control and documentation**

---

## Future Enhancements

* Integration with external data (Google Analytics, CRM data)
* Predictive retention modeling (using Python or R)
* Automated report refresh using Power BI Service and data gateways

---

## Author

**Ashkan Allahyari**
Business Analyst | Data Enthusiast | Power BI Developer
ashkan.allahyari@gmail.com



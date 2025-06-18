# Laundering Activity and Risk Assessment Dashboard (Power BI)

This Power BI dashboard helps simulate how suspicious transaction patterns might be identified in a financial system. Built using synthetic Anti Money Laundering Transaction Data (SAML-D), it allows interactive exploration of flagged activity, high-risk customer behavior, and individual transaction history.

PBIX File: [`/reports/AML_PBI_Dashboard.pbix`](./reports/AML_PBI_Dashboard.pbix)  
Screenshots: [`/images/`](./images) folder  
[Preview: Overview Page](https://github.com/JasmineShrestha11/Laundering-Activity-Report/blob/main/images/Overview.png)
---

## What This Dashboard Helps With

This dashboard supports financial crime analysts or auditors in identifying patterns of suspicious behavior, understanding customer risk profiles, and drilling down into transactional insights.

---

### Overview Page

**Helps answer:**
- What portion of total transactions or amounts are flagged as suspicious?
- Are flagged transactions or amounts increasing over time?
- Which categories contribute most to flagged activity?

**Interactive Features:**
- Toggle between **transaction count** and **amount** using the first slicer under **"Toggle Metric"**. This updates the donut, bar, and line charts accordingly.
- Use the second slicer to change the **X-axis category** in the bar chart, selecting from dimensions like **Payment Type**, **Laundering Type**, **Sender Location**, and more.

---

### Customer Risk Page

**Helps answer:**
- How many customers fall into each risk level (high, medium, low)?
- Who are the top 10 customers with the most flagged activity?
- What is the overall distribution of flagged activity across different risk groups?
- Do flagged activities involve large single transactions or multiple smaller ones?

**Interactive Features:**
- Toggle between **transaction count** and **amount** to update the bar chart and tree map.
- **Bar and scatter plots** are filtered by selected risk level.
- Selecting a bar or data point reveals the **"View Customer Details"** button, allowing navigation to the detailed view for that customer.

---

### Customer Details Page

**Helps answer:**
- What does this customer’s transaction pattern look like over time?
- How do flagged vs non-flagged transactions compare?
- Which categories dominate their behavior?

**Interactive Features:**
- Accessed via **drillthrough** from the Customer Risk page (bar or scatter chart selections).
- Toggle between **transaction count** and **amount** to update the line and bar charts.
- Change the **X-axis category** in the bar chart to explore dimensions such as **Payment Type**, **Laundering Type**, **Sender Location**, and more.
- Includes a detailed transaction table filtered for the selected customer.

---

<pre> <code>```text ## Project Structure Laundering-Activity-Report/ │ ├── reports/ │ └── LaunderingDashboard.pbix # Power BI report file │ ├── images/ │ ├── Overview.png # Dashboard page screenshots │ ├── CustomerRisk.png │ └── CustomerDetails.png │ ├── .gitattributes └── README.md # This file ```</code> </pre>

### Features & Techniques Used

- **Power BI DAX expressions** including `YTD`, `MTD`, and time intelligence functions
- **Field Parameters** to dynamically switch between metrics (transaction count or amount) and categories (e.g. payment type, laundering type)
- **Drillthrough navigation** from summary pages to detailed customer views
- **Interactive slicers** for dynamic exploration
- **Conditional formatting** and **KPI cards** to highlight flagged activities

## Dataset and References

This project uses the **Anti Money Laundering Transaction Data (SAML-D)** created for typology-based transaction monitoring:

- [Kaggle Dataset](https:https://www.kaggle.com/datasets/berkanoztas/synthetic-transaction-monitoring-dataset-aml)

**Citation:**
> B. Oztas, D. Cetinkaya, F. Adedoyin, M. Budka, H. Dogan and G. Aksu,  
> _"Enhancing Anti-Money Laundering: Development of a Synthetic Transaction Monitoring Dataset,"_  
> 2023 IEEE International Conference on e-Business Engineering (ICEBE), Sydney, Australia, pp. 47–54.  
> [DOI: 10.1109/ICEBE59045.2023.00028](https://ieeexplore.ieee.org/document/10356193)

---

## Notes

- This is a **project** built for learning Power BI and AML concepts.
- Dataset is fully synthetic, not tied to any real individuals or banks.

---


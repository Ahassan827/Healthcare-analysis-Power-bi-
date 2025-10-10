# Healthcare-analysis-Power-bi-

## 🎯 Objective

The goal of this analysis is to identify insights that highlight opportunities to improve hospital efficiency.  
Efficiency here means minimizing *waste* in time, cost, and resources — including equipment, supplies, and staff efforts.  
The analysis focuses on *Length of Stay (LOS)* and *Cost per Discharge* as the main performance indicators.

---


## 🧹 Data Cleaning (Power Query)
- Removed duplicates  
- Standardized data types (numeric, categorical, date)
- Filtered Rows → Kept only records where CCS Procedure Description = “HIP REPLACEMENT: TOT/PF” to focus the analysis on hip replacement cases.

---



## 📏 Measures Created 

The following DAX measures were created to calculate hospital efficiency indicators and enable dynamic comparisons between hospitals:

| **Measure Name** | **Description** |
|------------------|-----------------|
| **Average Cost per Discharge** | Calculates the average cost for each patient discharge by dividing total costs by total discharges. |
| **Average LOS Days** | Computes the average length of stay (LOS) for patients, indicating hospital efficiency in managing patient duration. |
| **% Var Average Cost per Discharge** | Shows the percentage variation of each hospital’s average cost per discharge compared to the overall average — helps identify cost efficiency gaps. |
| **% Var Average LOS Days** | Displays the percentage difference between each hospital’s average LOS and the overall average — used to detect performance deviations. |
| **Average Cost per Discharge ALL** | Calculates the overall (unfiltered) average cost per discharge for benchmarking. |
| **Average LOS Days ALL** | Calculates the overall (unfiltered) average LOS for comparison across hospitals. |
| **Total Discharges** | Counts the total number of patient discharges in the dataset. |
| **Total Hospitals** | Counts the number of unique hospitals included in the analysis. |
| **Total Surgeons** | Counts the number of distinct operating surgeons (based on license number). |
| **Title Selected Facility** | Creates a dynamic title showing the selected hospital name (e.g., “Hospital Profile: XYZ Hospital”). |


---


# 🏥 Hospital Efficiency Analysis — Insights & Recommendations

## 🎯 Objective

The goal of this analysis is to identify insights that highlight opportunities to improve hospital efficiency.  
Efficiency here means minimizing **waste** in time, cost, and resources — including equipment, supplies, and staff efforts.  
The analysis focuses on **Length of Stay (LOS)** and **Cost per Discharge** as the main performance indicators.

---

## 💡 Actionable Insights Extracted from the Data

### 1. Relationship Between LOS and Cost
Hospitals with a **high average LOS** tend to have a **higher cost per discharge**, as longer stays consume more medical resources and reduce bed turnover.  
However, some hospitals show **high LOS but low cost** (e.g., *Coney Island*, *Lincoln Medical*), suggesting that:
- The issue may stem from **administrative delays** or **discharge coordination problems**,  
- Rather than high medical or operational costs.

**Insight:** Not all hospitals with long stays are financially inefficient — some face **administrative or coordination delays** rather than poor clinical performance.

---

### 2. Severity of Illness as the Strongest LOS Driver
Patients classified under **“Extreme Severity”** stay approximately **9 days longer** on average, and those under **“Extreme Risk of Mortality”** stay **6 days longer**.  
This confirms that clinical severity is the **main driver** of longer hospital stays.

Improving efficiency doesn’t mean forcing shorter stays — it means:
- Managing critical cases more effectively.
- Allocating resources (ICU beds, staff) more efficiently.

**Insight:** Clinical severity is the dominant factor increasing LOS — hospitals should **optimize care pathways and resource use** rather than reduce stay time for critical cases.

---

### 3. Significant Financial Efficiency Variations
- Overall average cost per discharge: **$21K**  
- State Y average: **$26K**

This gap suggests **operational or administrative inefficiencies** between states, not only differences in patient complexity.  
Hospitals such as **United Memorial**, **St. Mary**, and **Newark** maintain **normal LOS** with **lower costs**.

**Insight:** Some hospitals achieve similar outcomes at significantly lower costs, revealing differences in **resource allocation and process efficiency**.

---

### 4. Double Waste: High LOS and High Cost
Hospitals like **King County**, **Memorial**, and **Interfaith** show both **high LOS** and **high costs**, making them top priorities for efficiency improvement.

**Insight:** Hospitals with both high LOS and cost represent **critical inefficiency zones** requiring urgent intervention.

---

### 5. Geographical Influence on Efficiency
Urban hospitals (especially in **New York City**) have an average LOS **1.68 days longer** than other regions, indicating higher demand and slower patient turnover.  
In contrast, non-urban regions such as **Southern Tier**, **Capital/Adirondack**, and **Central NY** demonstrate:
- Cost reductions of **$8.5K–$9K per discharge**.  
- Showing that **location and operational scale** affect efficiency.

**Insight:** Urban hospitals experience higher operational strain and slower flow, while rural hospitals achieve lower costs through **leaner systems and better resource balance**.

---

### 6. Mismatch Between Clinical and Operational Performance
Some hospitals maintain a **short LOS (~2.4 days)** but have **low discharge volumes**, indicating operational underutilization — possibly due to limited demand or narrow specialization.

**Insight:** Certain hospitals are **clinically efficient** but **operationally underused**, pointing to a need for broader service offerings or improved patient inflow management.

---

### 7. Key Factors That Increase Cost
Higher costs are associated with:
- Longer LOS and complex (extreme) cases  
- Urban location (especially NYC)  
- Poor discharge management and patient flow  
- Administrative inefficiencies and redundant procedures  
- Limited automation in billing and resource tracking  

---

### 8. Key Factors That Help Reduce Cost
Hospitals that successfully control costs typically:
- **Streamline patient discharge** through coordination with home care or rehab centers  
- **Use digital systems** for bed management, staff scheduling, and resource tracking  
- **Standardize clinical protocols** to reduce unnecessary variation  
- **Monitor departmental costs** to pinpoint high-expense areas  
- **Adopt value-based care**, focusing on outcomes instead of service volume  
- **Negotiate better supplier contracts** and minimize procurement waste  

**Insight:** Cost reduction is best achieved through **process optimization and digital efficiency**, not by cutting essential care resources.

---

## 🏆 Benchmark Example: Hospital for Special Surgery (HSS)

The **Hospital for Special Surgery (HSS)** stands out as a **benchmark of both operational and financial efficiency**.

| Metric | Performance |
|--------|--------------|
| Discharges | 26,000 |
| Average LOS | 2.65 days |
| Cost per Discharge | $20.91K (below average) |

**Key Success Drivers:**
- Focus on **low-to-moderate severity cases** (Minor/Moderate)  
- Clear specialization in **orthopedic and joint procedures**  
- Strong **discharge coordination** and post-surgery care planning  
- High **staff productivity** with optimized operating schedules  

**Insight:** HSS demonstrates how **specialization**, **efficient resource use**, and **effective discharge management** can reduce costs while maintaining high patient throughput and care quality.

---

## 🧭 Recommendations

### 1. Operational Improvements
- Adopt **digital discharge systems** to reduce bed occupancy delays  
- Implement **bed management dashboards** to monitor daily turnover  
- Share best practices from high-performing hospitals such as HSS  

### 2. Financial Optimization
- Conduct **cost audits** in high-cost hospitals (NYU, Memorial)  
- Apply **benchmark-based budgeting** using models from low-cost hospitals  
- Introduce **monthly cost-per-discharge tracking**  

### 3. Clinical Process Management
- Allocate **specialized teams** for high-severity cases to prevent LOS escalation  
- Introduce **severity-based treatment pathways** to streamline care  

### 4. Regional Strategy
- Replicate successful **rural efficiency models** in urban hospitals  
- Adjust **staffing and scheduling** in NYC hospitals to match demand peaks  

---

📊 **Overall Summary:**  
This analysis identifies operational inefficiencies, cost disparities, and best practices that can significantly enhance hospital performance.  
By applying targeted strategies — especially digital process automation and better resource coordination — hospitals can **reduce costs without compromising patient care**.

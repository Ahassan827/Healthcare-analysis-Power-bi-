# Healthcare-analysis-Power-bi-

## 🎯 Objective

The goal of this analysis is to identify insights that highlight opportunities to improve hospital efficiency.  
Efficiency here means minimizing *waste* in time, cost, and resources — including equipment, supplies, and staff efforts.  
The analysis focuses on *Length of Stay (LOS)* and *Cost per Discharge* as the main performance indicators.

## Business Problem:

Hip replacement surgeries across the state show significant variation in cost and LOS between hospitals — but it's unclear whether this variation is driven by clinical factors, operational inefficiencies, or both.

---


## 📊 Dataset Overview
- Number of rows : 26594
- Number of columns: 30
- Data Source: Datacamp



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



## 💡 Actionable Insights Extracted from the Data


## 1. Relationship Between LOS and Cost

Hospitals with high LOS tend to have higher costs. However, hospitals like Coney Island and Lincoln Medical show high LOS with low cost — suggesting the issue is administrative delays, not medical inefficiency.


💡 Insight: Not all hospitals with long stays are financially inefficient — some face coordination delays rather than poor clinical performance.


## 2. Severity of Illness as the Strongest LOS Driver

Extreme Severity patients stay ~9 days longer. Extreme Risk of Mortality patients stay ~6 days longer. Improving efficiency means managing critical cases better — not forcing shorter stays.


💡 Insight: Clinical severity is the dominant LOS driver — hospitals should optimize care pathways and resource allocation rather than reduce stay time for critical cases.


## 3. Significant Financial Efficiency Variations

Overall average cost per discharge: $21K

State Y average: $26K — a $5K gap per case

Hospitals like United Memorial, St. Mary, and Newark achieve similar outcomes at lower costs.


💡 Insight: Some hospitals achieve similar outcomes at significantly lower costs, revealing differences in resource allocation and process efficiency.


## 4. Double Waste: High LOS and High Cost
   
Hospitals like King County, Memorial, and Interfaith show both high LOS and high costs — making them the top priority for intervention.


💡 Insight: Hospitals with both high LOS and cost represent critical inefficiency zones requiring urgent action.


## 6. Geographical Influence on Efficiency

NYC hospitals average 1.68 days longer LOS. Non-urban regions like Southern Tier and Central NY show $8.5K–$9K lower cost per discharge.


💡 Insight: Urban hospitals face higher strain and slower flow, while rural hospitals achieve lower costs through leaner systems.


## 7. Mismatch Between Clinical and Operational Performance

Some hospitals have short LOS (~2.4 days) but very low discharge volumes — indicating operational underutilization.


💡 Insight: Certain hospitals are clinically efficient but operationally underused, pointing to a need for broader services or better patient inflow management.


## 8. Key Factors That Increase Cost

- Longer LOS and extreme severity cases
  
- Urban location (especially NYC)
  
- Poor discharge management and patient flow
  
- Administrative inefficiencies and redundant procedures
  
## 9. Key Factors That Help Reduce Cost

- Streamlined discharge coordination with home care and rehab centers
  
- Digital systems for bed management and staff scheduling
  
- Standardized clinical protocols
  
- Value-based care focused on outcomes over volume
  
💡 Insight: Cost reduction is best achieved through process optimization — not by cutting essential care resources.



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

🧭 Recommendations
## 1. Hospitals with High LOS but Low Cost (e.g., Coney Island, Lincoln Medical)

- The problem is administrative — not clinical.
 
 Action: Improve discharge coordination and post-surgery care planning.



## 2. Hospitals with High LOS and High Cost (e.g., King County, Memorial, Interfaith)

- These are the highest priority — double waste of time and money.
  
  Action: Start with a cost audit and apply the HSS operational model.


## 3. NYC Hospitals

- The problem is operational strain — not poor clinical performance.
   
  Action: Increase staffing during peak hours and optimize surgery scheduling.


## 4. Hospitals with Short LOS but Low Discharge Volumes
   
- Clinical efficiency exists — but it's not converting into real output.
  
  Action: Expand service offerings or improve patient inflow management.


## 5. State-wide

- HSS is the benchmark — clear specialization, strong discharge coordination, below-average cost.
  
  Action: Share HSS best practices across underperforming hospitals.
---

📊 **Overall Summary:**  
This analysis identifies operational inefficiencies, cost disparities, and best practices that can significantly enhance hospital performance.  
By applying targeted strategies — especially digital process automation and better resource coordination — hospitals can **reduce costs without compromising patient care**.



![WhatsApp Image 2025-11-11 at 10 03 54 PM](https://github.com/user-attachments/assets/e6a62d4c-6adf-4312-91b6-4e0bb810062f)



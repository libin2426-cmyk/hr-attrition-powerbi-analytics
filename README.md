# Strategic Workforce Analytics & Attrition Dashboard (Power BI)

##  Project Overview
An end-to-end HR analytics project analyzing 1,470+ employee records to identify core drivers of employee turnover, departmental vulnerability, and retention risks.

##  Dashboard Previews
![Attrition Overview](overview.png)
![Attrition Drivers](drivers.png)

##  Key Business Insights
- **High-Risk Tenure:** Employees in the 0–2 year tenure window exhibited the highest turnover rates.
- **Compensation & Overtime Impact:** Attrition spiked sharply among employees in lower salary bands (<$5k) working consistent overtime (74.7%).
- **Promotion Gaps:** Employees with a 6–10 year gap since their last promotion displayed elevated attrition likelihood.
- **Departmental Vulnerabilities:** Sales representatives and laboratory roles showed higher relative turnover compared to other business units.

##  Key DAX Formulas Used
- **Active Employees:**
  `Active Employees = CALCULATE(COUNT(HR_Data[EmployeeID]), HR_Data[Attrition] = "No")`
- **Inactive Employees:**
  `Inactive Employees = CALCULATE(COUNT(HR_Data[EmployeeID]), HR_Data[Attrition] = "Yes")`
- **Attrition Rate:**
  `Attrition Rate = DIVIDE([Inactive Employees], COUNT(HR_Data[EmployeeID]), 0)`

##  Repository Contents
- `HR_Analytics_Attrition.pbix`: Full Power BI desktop file with interactive data models and visuals.

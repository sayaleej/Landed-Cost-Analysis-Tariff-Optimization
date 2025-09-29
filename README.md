# Landed-Cost-Analysis-Tariff-Optimization

## 🎯 Project Overview

This project quantifies the impact of various tariffs (including HTS, Section 301/232, and IEEPA duties) and optimizes the Total Landed Cost for a product portfolio across multiple internal systems (Aircraft, Zip, and Dock).

The initial analysis was performed using an Excel framework to establish core metrics and demonstrate the potential for cost reduction and automation.

## 📊 Key Goals & Deliverables

The primary objective was to deliver a clear, actionable analysis of total import costs.

Cost Breakdown: Provided a detailed, system-level breakdown of Material, Freight, and Duty costs.

Effective Duty Estimates: Calculated the true effective duty rate on all imported components, considering country of origin (COO) and HTS codes.

Cost-Saving Strategies: Identified high-impact opportunities, such as HTS code reclassification (to legally reduce duty exposure) and disassembly/mode optimization (to lower freight/cost ratios).

Automation Proposal: Developed a comprehensive plan to migrate the manual framework to a scalable, automated BI solution.

### Data & Methodology
The analysis utilized structured data related to imported parts and a static tariff table.

### Data Sources
Dataset	Content	Key Fields
Raw data.csv -	Part-level details, costs, and origin.	Part Number, System, HTS Code, Country of Origin (COO), Material Cost, Freight Cost.

### Data Challenges & Preprocessing
A key step involved resolving data inconsistencies found across different systems (Zip and Dock) where freight and material costs were incorrectly assigned or labeled. An interpretation approach was applied to correct the unit costs, ensuring accurate landed cost calculations.

The Landed Cost Formula used the corrected Material Cost, Freight Cost, and the aggregated duty rate (HTS + Section 301/232/IEEPA + HMF/MPF fees).

## 🚀 Future Suggestions & Automation Roadmap
The analysis included a proposal to transition the manual Excel framework into a modern, scalable data solution, addressing limitations around interactivity and maintenance.

## Current Limitation	& Proposed Automation Solution
Manual Data Maintenance :	Automated HTS Duty Fetch using the official US ITC REST API using	Python (Requests), U.S. ITC HTS REST API
Static Reporting :	Migrate dashboards and calculations from Excel to a robust BI environment using	Power BI, Mode, or Tableau
Non-Real-Time Data :	Connect the analysis directly to the ERP and logistics systems using	SQL, ETL pipelines
Section 301/232 Updates	: Custom web scraping scripts for extracting data from official USTR notices (where no official API exists) using	Python (BeautifulSoup/Scrapy)

## 💡 Key Takeaways (Analysis Highlights)
Identified specific parts and origins with the highest Duty Impact (%).

Calculated Freight-to-Material Ratios to inform logistics optimization (e.g., favoring ocean/consolidated shipping for low-ratio items).

Provided tangible, data-backed evidence for prioritizing specific parts for HTS reclassification review.

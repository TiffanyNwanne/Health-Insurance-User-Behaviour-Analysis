# Medicare Utilisation Analysis

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Expenditure.png))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Expenditure.png)

## Project Background 

Medicare, the federal health insurance program for older adults and certain younger individuals with disabilities, continues to face mounting pressure to control costs while ensuring equitable access to care. Policymakers and healthcare leaders have raised critical concerns about the persistent geographic variation in Medicare spending and utilization — whether these differences reflect inefficiencies, population health disparities, or structural healthcare access issues.
This project is being led as part of a broader health policy and data science initiative aimed at understanding cost drivers and improving Medicare delivery nationwide. The analysis focuses on trends in average spending, utilization patterns, and demographic shifts over time — with an emphasis on identifying regions with atypical behavior, potential inefficiencies, and equity concerns.

This project involves cross-functional collaboration between:

- **Stakeholders (Health Policy Analysts & Program Managers):** Strategic guidance and interpretation for policy relevance

- **Data Analyst (Tiffany Nwanne):** Responsible for data cleaning, statistical analysis, and insights synthesis

- **Data Engineers & CMS Data Architects:** Supporting data access, validation, and technical infrastructure

### Stakeholder Questions Answered in This Analysis

- How has Medicare spending changed over time?

- Which states have the highest and lowest Medicare expenditures?

- What are the trends in inpatient vs. outpatient spending?

- How is Medicare Advantage (MA) enrollment growing?

- Which states have the highest emergency department (ED) visits and hospital readmissions?

- What are the racial/ethnic trends among Medicare beneficiaries?

## Dataset Description 
The dataset used for the analysis is the Medicare Fee-for-Service (FFS) Geographic Variation Public Use File (2014–2021). This dataset provides granular, region-level insights into Medicare expenditures, service utilization rates (e.g., hospitalizations, post-acute care, preventive services), and demographic characteristics of beneficiaries across the U.S.

The diagram is such as follows:
[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Tableau%20Joins.png))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Tableau%20Joins.png)


## Analysis and Insights 

SQL was used for data cleaning and analysis and then visualisation was done in Tableau.

### Medicare Expenditure

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Expenditure.png))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Expenditure.png)

This dashboard provides insights into Medicare spending trends across the United States, including year-over-year (YoY) growth, total spending over time, and average per capita spending. Additionally, it presents a hex map visualization of the average amount spent per state to highlight regional variations in Medicare expenditures.

**1️⃣ Year-Over-Year (YoY) Spending Growth**

The YoY spending growth rate is +3.5%, indicating a steady increase in Medicare expenditures.
This growth suggests rising healthcare costs, an aging population, or increased utilization of medical services.

**2️⃣ Total Medicare Spending Over Time**

The total Medicare spending has reached a massive $11 trillion.
This figure reflects cumulative spending over the years, underscoring the importance of Medicare in the healthcare system.

**3️⃣ Average Annual Medicare Spending Per Capita**

The average amount spent per Medicare beneficiary in a year is $84,476.
This metric helps gauge the cost burden per individual and highlights potential variations in healthcare costs by region.

**4️⃣ Geographic Spending Distribution (Hex Map Interpretation)**

The hex map provides a state-level breakdown of average Medicare spending per capita:

**High-Spending States:**

+ California (CA): $11,929
+ Texas (TX): $11,864
+ New Jersey (NJ): $12,918
+ Maryland (MD): $12,862
+ Connecticut (CT): $12,881
+ Washington D.C. (DC): $12,289

📝 These states have some of the highest per capita Medicare expenditures, likely due to higher healthcare costs, specialized medical centers, or larger elderly populations.

**Low-Spending States:** 

+ Montana (MT): $8,562
+ Idaho (ID): $8,901
+ Vermont (VT): $8,938
+ Maine (ME): $9,033
+ West Virginia (WV): $9,522

  
📝 These states tend to have lower Medicare spending per capita, which could be due to lower healthcare costs, fewer medical facilities, or healthier aging populations.

### Medicare Utilization

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Utilization.png))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Utilization.png)

This dashboard provides a comprehensive overview of how Medicare beneficiaries utilize healthcare services. It includes insights into Medicaid dual eligibility for Medicaid, inpatient vs. outpatient spending, total Medicare enrollment, and Medicare Advantage growth.

**1️⃣ Medicaid Dual Eligibility (%)**

+ Top KPI Tile: Displays the percentage of Medicare beneficiaries also eligible for Medicaid (30%).
+ Line Chart: Shows trends in dual eligibility over time, with a slight decrease in recent years.

**Insight:**

- A declining dual eligibility rate suggests that fewer Medicare beneficiaries are qualifying for Medicaid, which could be due to income shifts or policy changes affecting Medicaid eligibility.

**2️⃣ Inpatient vs. Outpatient Spending**

- Top KPI Tile: Shows the breakdown of Medicare expenditures:
- 97% spent on inpatient care
- 3% spent on outpatient care
- Bar Chart: Illustrates how annual spending is distributed between inpatient and outpatient services.

**Insight:**
- Inpatient care dominates Medicare spending, accounting for the majority of costs.
- Outpatient spending is minimal, possibly due to lower costs per service and fewer hospitalizations as medical practices shift towards ambulatory and home care services.

**3️⃣ Total Medicare Beneficiaries**

**Top KPI Tile:**

Highlights the total number of Medicare beneficiaries (88 million).

**Insight:**

- Medicare enrollment continues to rise, driven by aging baby boomers and expansion of Medicare Advantage plans.

4️⃣ Growth in Medicare Advantage Enrollment

Area Chart: Shows rapid growth in Medicare Advantage enrollment, surpassing 100 million in recent years.

**Insight:**

- Medicare Advantage plans are becoming more popular, likely due to expanded coverage options, lower out-of-pocket costs, and additional benefits (e.g., dental, vision, wellness programs).This growth suggests a shift away from traditional Medicare as more beneficiaries opt for private insurers managing Medicare coverage.

## Medicare Demographics

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Demographic.png))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Hot%20Spots.png)

This dashboard provides insights into the demographic distribution of Medicare beneficiaries, including race, gender, and age. These factors are crucial in understanding the makeup of Medicare recipients and how policies might affect different populations.

**1️⃣ Racial Demographics**

**Top KPI Tile:**

Shows that White beneficiaries make up 79% of the Medicare population.

**Bar Chart:**

- Black beneficiaries account for 10% of enrollees.
  
- Hispanic beneficiaries make up 6%, but their numbers are rising.
  
- Other racial groups represent 5% of Medicare enrollees.

**Insight:**

- Medicare is still overwhelmingly utilized by White beneficiaries (79%), but there's a gradual increase in Hispanic and Other racial groups.This suggests changing population demographics and the need for culturally tailored healthcare programs.

**2️⃣ Gender Distribution**

**Top KPI Tile:** Medicare is 53% female and 47% male.

**Trend Charts:** Show the historical progression of female and male participation in Medicare from 2013 to 2022.

**Insight:**

- Women slightly outnumber men in Medicare, likely due to longer life expectancy.
- Over time, the male participation rate has been increasing, suggesting improving healthcare access and life expectancy for men.

3️⃣ Average Age of Medicare Beneficiaries

Top KPI Tile: The average age of Medicare enrollees is 66 years.

**Insight:**

- This indicates a steady influx of new enrollees as people become eligible at age 65.

- Policy changes affecting eligibility (e.g., raising the retirement age) could significantly impact this metric in the future.

## Hot Spots

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Hot%20Spots.png))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Hot%20Spots.png)

This dashboard identifies states with the highest rates of critical healthcare issues, such as readmissions, hospitalizations due to diabetes, and emergency department visits. These metrics highlight areas with significant healthcare burdens, guiding policy decisions and resource allocation.

### States with Highest Readmissions

**Top KPI Tile:** District of Columbia (DC) leads with 869M readmissions.

**Bar Chart:**

- DC (869M) has the highest readmissions.

- Massachusetts (MA) follows with 766M.

- Maryland (MD) and New York (NY) also report high numbers.

**Insight:**

- High readmission rates indicate potential issues with post-discharge care and hospital efficiency.

- DC’s extreme readmission rate suggests possible healthcare access problems or patient demographic challenges.

### States with Highest Hospitalization from Diabetes

**Top KPI Tile:** Florida (FL) has the most diabetes-related hospitalizations (327 cases).

**Bar Chart:**

- FL (327), LA (308), and IN (304) lead in diabetes hospitalizations.

- Connecticut (CT) and Illinois (IL) also report high cases (~300 each).

**Insight:**

- Southern states dominate this metric, indicating that diabetes prevalence is a major issue in the region.

- Preventative care efforts (e.g., lifestyle programs, diet initiatives) might be underfunded or ineffective in these areas.

- States with high diabetes hospitalization rates might also struggle with obesity and access to primary care.

### States with Highest Emergency Department Visits

Top KPI Tile: California (CA) has the most ER visits, with 4,252 per 1,000 patients.

**Bar Chart:**

CA (4,252), TX (3,522), FL (3,574), MI (3,632), and PA (3,492) are the top five states.

**Insight:**

- Emergency department overuse often signals inadequate primary care access.

- California’s high ER visit rate suggests potential overburdened hospitals and limited availability of urgent care clinics.

- Florida and Texas also show high ER utilization, which could be due to high uninsured populations.

**Key Takeaways from the Hot Spots Dashboard**

- DC has the highest readmission rate (869M)—indicating possible healthcare access and efficiency issues.
- Florida leads in diabetes-related hospitalizations (327 cases)—highlighting chronic disease prevalence.
- California has the highest ER visits (4,252 per 1,000)—potentially pointing to gaps in primary care.












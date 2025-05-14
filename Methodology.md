# Methodology
These are the SQL queries that were used to clean and analse the Medicare dataset.

## Data Import

The dataset was downloaded from the CMS Data Portal ([data.cms.gov](https://data.cms.gov)) as an Excel file.

The dataset was converted to **CSV** using **Microsoft Excel**.

## Database Creation

Using **SQLite Studio**, I created a database named `medicare_data.sqlite` and a table based on the data dictionary.

Once the table was created, the CSV file was imported into SQLite using:

```sql
```sql
.mode csv
.import Medicare_FFS_Geographic_Variation.csv medicare_variation
'''''
```

## Initial Data Exploration

**Annual Medicare Spending Trends**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Annual%20Medicare%20Spending%20Trends.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Annual%20Medicare%20Spending%20Trends.JPG)

**📝 Findings:** Medicare spending has increased annually, with per capita spending also rising.

## Data Cleaning

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Checking%20Unique%20Regions.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Checking%20Unique%20Regions.JPG)

The dataset contains both states and cities (HRRs), making it difficult to extract state-level information.


[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Extracting%20State%20Abbreviations.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Extracting%20State%20Abbreviations.JPG)

The first two characters of bene_geo_desc were correspond to state abbreviations, which I used in later queries.

## Analysis

**1️⃣ State-Level Medicare Spending**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/State-Level%20Medicare%20Spending.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/State-Level%20Medicare%20Spending.JPG)

**📝 Findings:** **California, Texas, Florida, and New York** have the highest Medicare spending.

**2️⃣ Inpatient vs. Outpatient Spending Trends**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Inpatient%20vs.%20Outpatient%20Spending%20Trends.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Inpatient%20vs.%20Outpatient%20Spending%20Trends.JPG)

**📝 Findings:** Outpatient spending is increasing, suggesting a shift toward preventive care**.

**3️⃣ Growth in Medicare Advantage Enrollment**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Growth%20in%20Medicare%20Advantage%20Enrollment.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Growth%20in%20Medicare%20Advantage%20Enrollment.JPG)

**📝 Findings:** Medicare Advantage enrollment is growing, reducing reliance on FFS Medicare.

**4️⃣ Hospital Readmission Trends**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Hospital%20Readmission%20Trends.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Hospital%20Readmission%20Trends.JPG)

**Top 5 States with Highest Hospital Readmission Rates**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Top%205%20States%20with%20Highest%20Hospital%20Readmission%20Rates.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Top%205%20States%20with%20Highest%20Hospital%20Readmission%20Rates.JPG)

**📝 Findings:** Some states have consistently high readmission rates, indicating care quality issues.


**5️⃣ Racial & Ethnic Breakdown**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Racial%20%26%20Ethnic%20Breakdown.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Racial%20%26%20Ethnic%20Breakdown.JPG)

**📝 Findings:** White beneficiaries remain the majority, but Hispanic and Black enrollment is increasing.


**6️⃣ Dual-Eligible Beneficiaries (Medicare + Medicaid)**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Dual-Eligible%20Beneficiaries%20(Medicare%20%2B%20Medicaid).JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Dual-Eligible%20Beneficiaries%20(Medicare%20%2B%20Medicaid).JPG)

**7️⃣ Gender and Age Distribution**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Gender%20and%20Age%20Distribution.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Gender%20and%20Age%20Distribution.JPG)

**8️⃣ Top 5 States with Highest Diabetes Hospitalization Rates**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Top%205%20States%20with%20Highest%20Diabetes%20Hospitalization%20Rates.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Top%205%20States%20with%20Highest%20Diabetes%20Hospitalization%20Rates.JPG)

**9️⃣ Top 5 States with Highest Dmergency Department (BD) Usage**

[![Preview Image](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Top%205%20States%20with%20Highest%20Dmergency%20Department%20(BD)%20Usage.JPG))](https://github.com/TiffanyNwanne/Medicare-Utilisation-Analysis-By-Geography/blob/main/images/Top%205%20States%20with%20Highest%20Dmergency%20Department%20(BD)%20Usage.JPG)

**📝 Findings:** The number of **low-income beneficiaries (Medicare + Medicaid) is rising**.

The data was then exported as a csv file to Tableau for visualization 

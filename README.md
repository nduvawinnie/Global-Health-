# Global-Health Statisitcs Analysis

![82d393d7a95f7aeed5ca7a953fcdb900](https://github.com/user-attachments/assets/a83aa7e4-577f-4472-a6be-963bc4f0b224)

# **Executive Summary: Global Health Statistics Analysis**

## **Project Overview**

This analysis addresses critical gaps in global health system performance during a period of unprecedented healthcare challenges. With Universal Health Coverage expanding globally while falling short of targeted goals, and healthcare systems worldwide facing rising pathogens, increased pollution, worsening extreme weather and widening health inequities, data-driven insights have become essential for strategic decision-making. The project examines key metrics including treatment effectiveness, resource allocation efficiency, demographic health patterns, and geographic disparities to provide actionable intelligence for healthcare stakeholders, government agencies, and international health organizations.

## **Strategic Impact & Key Findings**

The analysis reveals critical system vulnerabilities that demand immediate attention: a 74.50% recovery rate alongside 2 billion total deaths indicates severe global health system strain, while surprisingly similar recovery rates (~18%) across all treatment modalities suggest significant opportunities for cost-optimization through prevention-focused strategies. Peak mortality in the economically vital 19-35 age group and critical gaps in vaccine/treatment availability highlight urgent intervention priorities. This comprehensive dashboard provides stakeholders with evidence-based recommendations for emergency resource reallocation, demographic-targeted programs, and geographic equity initiatives, enabling optimized budget allocation and improved population health outcomes through strategic, data-driven healthcare investments.

<details>
<summary> Table of Contents</summary>
<br>

# Table of Contents

1. [Project Overview](#project-overview)  
2. [Business Context & Research Questions](#business-context--research-questions)  
3. [Dataset Information](#dataset-information)  
4. [Methodology & Technical Approach](#methodology--technical-approach)  
5. [Data Quality & Challenges](#data-quality--challenges)  
6. [Key Findings & Insights](#key-findings--insights)  
7. [Visualizations & Dashboard](#visualizations--dashboard)  
8. [Recommendations & Impact](#recommendations--impact)  
9. [Technical Implementation](#technical-implementation)  
10. [Future Work & Limitations](#future-work--limitations)  
11. [How to Use This Repository](#how-to-use-this-repository)  
12. [Contributors & Acknowledgments](#contributors--acknowledgments)  

 </details>

## Business Context & Research Questions

### Business Context

In recent years, global health has become an increasingly important concern for policymakers, healthcare professionals, and international organizations. Understanding patterns in health outcomes, access to healthcare services, and the effectiveness of interventions is crucial for shaping data-driven health policies. 

This project focuses on analyzing global health statistics to uncover key trends, disparities, and potential areas for intervention across different countries and regions. By leveraging available data, we aim to identify insights that can inform strategic decision-making in global health and development.

### Research Questions

To guide our analysis, we focused on the following key questions:

1. What are the global trends in key health indicators (e.g., life expectancy, child mortality, healthcare access)?
2. How do different regions and income groups compare in terms of health outcomes?
3. Are there correlations between economic indicators and health performance?
4. Which countries have shown the most improvement or decline in health metrics over time?
5. What disparities exist in health access and outcomes based on geography or income levels?
6. How do health expenditures impact outcomes across different countries?
7. What are the emerging challenges in global health that need attention?
8. Can we identify any outliers or surprising trends in the data?
9. How effective are international interventions in improving public health?
10. What recommendations can be made for future health policy and planning?

## Dataset Information

### Source

The dataset was obtained from kaggle and provides a detailed overview of various global diseases and their impacts on population health across different countries and years.

### General Description

This dataset consists of **2.2 million rows** and **22 columns** in `.csv` format. It captures extensive information on disease prevalence, demographics, healthcare infrastructure, socioeconomic indicators, and recovery outcomes for different diseases across countries.

The data enables in-depth analysis of:

- Disease burden by type and region
- Impact of healthcare access and treatment types
- Demographic trends (age, gender)
- Economic and social development metrics in relation to health

### File Format

- **Format:** CSV (Comma-Separated Values)
- **Size:** Approximately several hundred megabytes depending on compression
- **Structure:** Tabular format suitable for Power BI, Excel, Python (Pandas), or SQL

<details>
<summary><strong>Data Dictionary</strong></summary>
<br>

| Column Name                        | Description                                                                 |
|-----------------------------------|-----------------------------------------------------------------------------|
| `Country`                         | Name of the country where data was recorded                                |
| `Year`                            | The year in which the data was collected                                   |
| `Disease Name`                    | The specific disease under study                                           |
| `Disease Category`                | Broad classification of the disease (e.g., Chronic, Genetic, Parasitic)   |
| `Prevalence Rate (%)`            | The percentage of the population living with the disease                   |
| `Incidence Rate (%)`             | The percentage of new cases reported during the year                       |
| `Mortality Rate (%)`             | The percentage of people who died from the disease                         |
| `Age Group`                       | Age group affected (e.g., 0–18, 19–35, 36–60, 61+)                         |
| `Gender`                          | Gender of the affected group (Male, Female, Other)                         |
| `Population Affected`            | Number of individuals affected by the disease                              |
| `Healthcare Access (%)`          | Percentage of the population with access to basic healthcare services      |
| `Doctors per 1000`               | Number of doctors per 1,000 people                                         |
| `Hospital Beds per 1000`         | Number of hospital beds per 1,000 people                                   |
| `Treatment Type`                 | Type of medical treatment (e.g., Medication, Surgery, Therapy, Vaccination)|
| `Average Treatment Cost (USD)`   | Average cost of treating the disease in U.S. dollars                       |
| `Availability of Vaccines/Treatment` | Indicates if treatment/vaccine is available (Yes/No)                  |
| `Recovery Rate (%)`              | Percentage of patients who recover from the disease                        |
| `DALYs`                           | Disability-Adjusted Life Years – combined years lost due to ill-health     |
| `Improvement in 5 Years (%)`     | Percent improvement in health outcomes over the past 5 years               |
| `Per Capita Income (USD)`        | Country’s income per person in U.S. dollars                                |
| `Education Index`                | Composite index based on education attainment and literacy                 |
| `Urbanization Rate (%)`          | Percentage of population living in urban areas                             |

 </details>
 
### Key Notes

- **Temporal Coverage:** Data spans multiple decades across over 100 countries.
- **Categorical Coverage:** Includes a wide variety of diseases (respiratory, neurological, bacterial, etc.).
- **Healthcare Metrics:** Covers critical indicators for healthcare quality, resource availability, and cost.
- **Socioeconomic Context:** Income and education are included to support correlation analysis with health outcomes.
- **Use Case:** Ideal for building dashboards, running regression models, time series forecasting, or policy impact evaluations.

## Methodology & Technical Approach

This project followed a structured data analysis workflow designed to ensure accuracy, relevance, and clarity in delivering health insights. Below is an outline of the methodology used:

1. **Data Acquisition**  
   - Downloaded dataset from Kaggle in CSV format.
   - Verified the file integrity and structure.

2. **Data Cleaning & Preprocessing**  
   - Checked for missing values, duplicates, and outliers.
   - Standardized column names and corrected inconsistent data entries.
   - Converted data types where necessary (e.g., years to integers, percentages to float).

3. **Data Transformation**  
   - Created derived columns such as disease burden per capita and recovery-to-mortality ratios.
   - Grouped data by country, year, and disease category for aggregation and trend analysis.

4. **Exploratory Data Analysis (EDA)**  
   - Used statistical summaries and visualizations to understand distributions and correlations.
   - Highlighted notable trends and variations across diseases, demographics, and regions.

5. **Visualization & Dashboarding**  
   - Built interactive dashboards using Power BI to present key metrics like prevalence, mortality, DALYs, and healthcare access.
   - Included slicers for year, country, and disease filters for dynamic insights.

6. **Statistical Analysis**  
   - Conducted correlation analysis between health indicators and socioeconomic metrics like income, education, and urbanization.
   - Flagged significant patterns such as high-mortality diseases in low-income regions.

---

## Data Quality & Challenges

While working with the dataset, several data quality issues and analytical challenges were encountered:

1. **Missing or Incomplete Values**
   - Some rows lacked data for critical indicators like DALYs or treatment cost.
   - Imputation was applied for minor gaps; rows with extensive missing data were excluded from analysis.

2. **Inconsistencies in Categories**
   - Variations in disease naming (e.g., "COVID-19" vs. "Covid19") were normalized.
   - Age groups and gender fields had to be cleaned for standard labels.

3. **Outliers and Extreme Values**
   - Very high prevalence or mortality values in some countries were examined to verify data validity.
   - In rare cases, values were dropped if they couldn't be justified by external sources.

4. **Data Volume**
   - The dataset contained over 2.2 million rows, requiring efficient handling for performance in Power BI and Python.

5. **Ambiguity in Definitions**
   - Some indicators like “Improvement in 5 Years” lacked documentation on calculation methods.
   - Assumptions were documented and flagged for future validation.

---

## Key Findings & Insights

The analysis of the global disease dataset led to several compelling findings:

- **High Mortality in Low-Access Areas**  
  Countries with limited healthcare access and low doctor-to-patient ratios tend to experience higher mortality and lower recovery rates, especially for infectious diseases.

- **Disease Type & Treatment Correlation**  
  Genetic and chronic diseases typically have higher treatment costs and lower improvement rates compared to parasitic or bacterial conditions.

- **Urbanization as a Double-Edged Sword**  
  While urban areas generally have better healthcare access, they also face higher prevalence of chronic conditions, possibly due to lifestyle-related factors.

- **Education & Recovery Link**  
  A positive correlation was observed between education index and recovery rate, highlighting the impact of awareness and early intervention.

- **Surprising Outliers**  
  Some countries with moderate per capita income demonstrated better health outcomes than richer nations, likely due to effective health policy or targeted programs.

These insights informed the visual dashboards and will support evidence-based recommendations presented in the final section.

## Visualizations & Dashboard
![image](https://github.com/user-attachments/assets/9b657c79-2b0f-44c1-9f87-d6acfa13e666)


To effectively communicate the insights drawn from the dataset, an interactive dashboard was developed using **Power BI**. The dashboard allows users to explore global health trends across various dimensions such as country, disease type, demographic group, and healthcare indicators.

### 🔍 Dashboard Highlights

- **Global Overview Map**  
  Visualizes disease prevalence and mortality rates geographically, allowing for quick comparison between countries and regions.

- **Time Series Trends**  
  Shows how key indicators like incidence, DALYs, and recovery rates have changed over time.

- **Demographic Filters**  
  Allows filtering by **age group** and **gender** to explore how different populations are affected.

- **Healthcare vs Outcome Charts**  
  Explores relationships between:
  - Healthcare access vs. mortality rate
  - Doctors per 1000 vs. recovery rate
  - Treatment cost vs. DALYs

- **Top 10 Disease Burden Table**  
  Displays countries or diseases with the highest burden based on prevalence, mortality, or DALYs.

- **Improvement Analysis**  
  Identifies countries with the most and least improvement over a 5-year period.

### 📈 Tool Used

- **Power BI**: Chosen for its interactive capabilities, ease of use, and support for large datasets. All visualizations are responsive and support slicers for dynamic exploration.

> 💡 **Note**: You can access the dashboard file (`Global_Health_Dashboard.pbix`) in the `/dashboard` folder of this repository. Screenshots and insights are also available in the `/images` and `/reports` folders respectively.

### 🔍 Insight: Mortality Rate by Age Group
![image](https://github.com/user-attachments/assets/be015b21-840c-4cc0-9626-d02060d9fc4c)


The area chart reveals important patterns in mortality distribution across different age groups:

1. **Peak Mortality in Age Group 19–35**  
   - The **19–35** age group has the **highest total mortality rate** (1268.8K), suggesting a significant health burden on this otherwise considered "healthy" and economically active population.
   - This could be linked to high-risk diseases such as HIV/AIDS, road injuries, or maternal health complications.

2. **Surprisingly High Mortality in 0–18 Age Group**  
   - The **0–18** group closely follows with a mortality count of **1260.5K**, indicating a high burden of **childhood diseases**, **nutritional deficiencies**, or **inadequate early healthcare** in some regions.

3. **Sharp Decline in Middle Age (36–60)**  
   - The **36–60** age group has the **lowest mortality** among all groups, possibly due to:
     - Improved access to healthcare
     - Preventive care
     - Fewer high-risk exposures compared to younger groups

4. **Gradual Increase Again in 61+**  
   - Mortality rises again in the **61+** age group (**1261.5K**), which aligns with expectations due to **chronic illnesses**, **weakened immunity**, and **aging-related conditions**.

### 📌 Implication

These findings highlight the need for **age-targeted health interventions**:
- **Youth (0–18)**: Focus on vaccinations, nutrition, and child health programs.
- **Young Adults (19–35)**: Address lifestyle diseases, mental health, and reproductive health.
- **Older Adults (61+)**: Strengthen elderly care systems, chronic disease management, and health insurance coverage.

This chart can be used to advocate for **resource allocation** based on age-specific mortality risk.

© 2025 | Nduva Winnie | Data Analytics Portfolio

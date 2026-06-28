# Teen Pregnancy Analysis

## Table of Content
1. [Project Overview](#project-overview)
2. [Data Sources](#data-sources)
3. [Tools](#tools)
4. [Data Cleaning/Preparation](data-cleaning/preparation)
5. [Exploratory Data Analysis](#exploratory-data-analysis)
6. [Data Analysis](#data-analysis)
7. [Results/Findings](results/fingings)
8. [Recommendations](#recommendations)
9. [Limitations](#limitations)

    
### Project Overview

This data analysis project examines teen pregnancy trends in Kenya. It aims to identify patterns, highlight counties with the highest and lowest rates, and provide data-driven insights to support informed decision-making.

### Data Sources

Teen pregnancy data was extracted from:
1.	Kenya National Bureau of Statistics (KNBS)
2.	Kenya Economic Survey
3.	United Nations Population Fund (UNFPA) Kenya
4.	National Council for Population and Development
5.	 World Bank Open Data
6.	United Nations Development Programme

 ### Tools

- Excel - Data Cleaning
-	SQL Server – Data Analysis
-	Tableau – Creating Reports

### Data Cleaning/Preparation

In the initial data preparation phase, the following tasks were performed:
1.	Data loading and inspection
2.	Data Cleaning and formatting

### Exploratory Data Analysis

The exploratory data analysis examined teen pregnancy data in Kenya to answer key questions such as:
-	What is the overall trend in teen pregnancy?
-	Which counties have the highest and lowest teen pregnancy?
-	Which factors were the major contributors to high or low teen pregnancy?
-	Were the mitigation measures working?

### Data Analysis

Include the following code features worked with

```sql
SELECT 
    county,
    CORR (Teen_pregnant_pct, poverty_pct) AS correlation
FROM (
    SELECT 
        t.county,
        t.year,
        t.Teen_pregnant_pct,
        p.poverty_pct
    FROM teen_pregnancy t
    JOIN poverty_rates p 
        ON t.county = p.county AND t.year = p.year
) x
GROUP BY county;
```

Excel – Conducted Correlation and regression analysis to access key drivers.
   - [Download here](https://1drv.ms/x/c/34521100c0fad225/IQArzmdBoiNPS4NS-sG6wke4AbQExMc90JpNaB2grPYOiHM?e=Emr3ql)


### Results/Findings

The analysis results are summarized as follows:
-	Identified a positive correlation between poverty and teenage pregnancy until 2021, after which poverty rose while teenage pregnancy declined — suggesting the impact of targeted interventions.
-	Compared top 5 high-prevalence counties with top 5 low-prevalence counties, revealing that low-prevalence areas had lower poverty rates, higher literacy levels, and greater access to contraception.


### Recommendations

-	Scale Up Youth Friendly Sexual and Reproductive Health (SRH) Service.
-	 Enhance Community Engagement and Behaviour Change Communication through partnership with cultural and religious leaders to address norms around early marriages.
-	 Strengthen Monitoring, Evaluation, and Learning (MEL) Systems to track and identify progress gaps.
-	 Conduct Further Research on the Post 2021 Decline to investigate which interventions contributed most to the decline in teen pregnancy.

### Limitations

-	Limited county data for teen pregnancy. Projected data by UNFPA Kenya was used for 20% of the study




















































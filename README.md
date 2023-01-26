# ICU Readmission Prediction

This repository contains code files used to predict ICU readmissions from a large clinical dataset (PMAP) collected at Johns Hopkins Hospital (JHH).

## Project Background

This project aims to predict readmissions that occur 1-30 days after a Congestive Heart Failure (CHF) - related ICU hospital stay.

## Project Contents
### Code (Python Notebooks)

**1. Defining our target cohort**
  - PMAP_Final_Cohort: This file first identifies our targeted cohort (CHF-related ICU hospital stays), then generates labels for each hospital stay. The below diagram shows a summary of how the cohort is extracted.

![image](https://www.linkpicture.com/q/PMAP-final-cohort.png)

**2. Feature Engineering**
  - PMAP_Comorbidity: This file reads in diagnosis information (ICD-10 codes) from hospital billing and diagnosis data, performs data cleaning procedures, then finally generates features including Charlson and Elixhauser Comorbidity Indexes, and Elixhauser scores.
  - PMAP_Demographic: This file reads in patient demographic information, then generates demographic features including age, gender, and race.
  - PMAP_Labs:

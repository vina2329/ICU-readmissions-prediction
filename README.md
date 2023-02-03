# ICU Readmission Prediction

This repository contains code files used to predict ICU readmissions from a large clinical dataset (PMAP) collected at Johns Hopkins Hospital (JHH).

## Project Background

This project aims to predict readmissions that occur 1-30 days after a Congestive Heart Failure (CHF) - related ICU hospital stay.

## Project Contents
### Code (Python Notebooks)
**0. Loading Files from S drive to PMAP crunchr platform**
  - PMAP_ld_fr_Sdrive: This file directly loads large files directly from the S drive of SAFE Desktop to the crunchr platform.

**1. Defining our target cohort**
  - PMAP_Final_Cohort: This file first identifies our targeted cohort (CHF-related ICU hospital stays), then generates labels for each hospital stay. The below diagram shows a summary of how the final cohort is extracted out of each hospital stay in our dataset.

![image](https://www.linkpicture.com/q/PMAP-final-cohort.png)

**2. Feature Engineering**
  - PMAP_Comorbidity: This file reads in diagnosis information (ICD-10 codes) from hospital billing and diagnosis data, performs data cleaning procedures, then finally generates the Elixhauser Comorbidity Index.
  - PMAP_Demographic: This file reads in patient demographic information, then generates demographic features including age, gender, and race.
  - PMAP_Labs:
  - PMAP_Meds:This file reads in medication administrations for every hospital stay, then generates medication features including med classes administered for each of our target hospital stay and the average dosages/patient weight/min given.
    - PMAP_get_pat_weights: This file pulls the weights of patients from patient flowsheets to calculate average dosages/patient weight/min given.

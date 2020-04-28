# DIABETES READMISSION AND EFFECTIVE TREATMENT PREDICTION 

## CONTENTS
1. Objective
2. Smart Question
3. Introduction
4. Data
5. Summary
6. Method/Code Contents
7. Appendix

## OBJECTIVE
The purpose of this report is to identify whether a patient will be readmitted in some hospital and the possible treatment given to the patient in order to change the treatment, to avoid a readmission.

## SMART QUESTION:
To Predict the early readmission of diabetic patients and to predict the effective treatment given to a diabetic patient based on various features like Race, gender, age, Medication, A1CResults, etc.

## INTRODUCTION
Diabetes and complications, deaths, and societal costs associated with diabetes have a huge and rapidly growing impact on the United States. Between 1990 and 2010 the number of people living with diabetes tripled and the number of new cases annually doubled. Hence hospital readmission of diabetic patients has become a high-priority health care quality measure and target for cost reduction, particularly within 30 days of discharge also called as 30-day readmission/early readmission. Rubin, D.J. in his article about Hospital Readmission of Patients with Diabetes says the burden of diabetes among hospitalized patients, is substantial, growing, and costly, and readmissions contribute a significant portion of this burden. Factors such as male gender, comorbidity burden, hospital length of stay, government insurance vs. private or no insurance, emergent or urgent vs. elective admission, recent prior hospitalization, and being discharged against medical advice are associated with an increased risk of 30-day readmission. Hospitalized patients with diabetes may be at higher risk of readmission than those without diabetes. Despite broad interest in readmission, relatively little research has focused on patients with diabetes. Hence, reducing readmission rates among patients with diabetes has the potential to greatly reduce health care costs while simultaneously improving care.

## DATA
In this study we have used Diabetes 130 US hospitals for years 1999-2008 dataset from Kaggle [(link)](https://www.kaggle.com/brandao/diabetes). The main source for this data set is UCI Machine Learning Repository [(link)](https://archive.ics.uci.edu/ml/datasets/Diabetes+130-US+hospitals+for+years+1999-2008). The data are submitted on behalf of the Center for Clinical and Translational Research, Virginia Commonwealth University. The dataset represents 10 years (1999-2008) of clinical care at 130 US hospitals and integrated delivery networks. It includes over 50 features representing total of 101,766 patient and hospital outcomes. The size of the dataset is 18MB. The data contains attributes such as patient number, race, gender, age, admission type, time in hospital, medical specialty of admitting physician, number of lab test performed, HbA1c test result, diagnosis, number of medication, diabetic medications, number of outpatient, inpatient, and emergency visits in the year before the hospitalization, etc. refer to Data Dictionary in appendix for more details.
    
## Summary:
With the increasing number of diabetic patients in US it is important to consider the readmissions of the patients to the hospitals within 30 days of discharge and the treatments given to them as early readmission adds burden of penalty to the hospitals. This project provides thorough analysis of factors that might affect early readmission of the patients using method like Random Forest for feature importance. Further it provides the prediction of whether the patient will be early readmitted, and the possible treatments given in early cases using Diabetes 130 US hospitals for years 1999-2008 dataset and by making use of various supervised machine learning algorithms in order to reduce rate of early readmission in the future.
    
## METHOD/CODE CONTENTS:
1. Data Preprocessing
2. Feature Engineering - Part 1
3. Exploratory Data Analysis
4. Feature Engineering - Part 2
5. Target - Readmission
   - Getting the Features
   - Hyperparameter Tuning
   - Model Selection
6. Target - Treatment
   - Getting the Features
   - Hyperparameter Tuning
   - Model Selection

## REFERENCES:
1. Beata Strack, Jonathan P. DeShazo, Chris Gennings, Juan L. Olmo, Sebastian Ventura, Krzysztof J. Cios, and John N. Clore, “Impact of HbA1c Measurement on Hospital Readmission Rates: Analysis of 70,000 Clinical Database Patient Records,” BioMed Research International, vol. 2014, Article ID 781670, 11 pages, 2014.
2. Rubin, D.J. Hospital Readmission of Patients with Diabetes. Curr Diab Rep 15, 17 (2015). https://doi.org/10.1007/s11892-015-0584-7

## APPENDIX [DATA DICTIONARY]:
1. Encounter ID Unique identifier of an encounter
2. Patient number Unique identifier of a patient
3. Race Values: Caucasian, Asian, African American, Hispanic, and other
4. Gender Values: male, female, and unknown/invalid
5. Age Grouped in 10-year intervals: 0, 10), 10, 20), …, 90, 100)
6. Weight in pounds (missing 97%)
7. Admission type Integer identifier corresponding to 9 distinct values, for example, emergency, urgent, elective, newborn, and not available
8. Discharge disposition Integer identifier corresponding to 29 distinct values, for example, discharged to home, expired, and not available
9. Admission source Integer identifier corresponding to 21 distinct values, for example, physician referral, emergency room, and transfer from a hospital
10. Time in hospital Integer number of days between admission and discharge
11. Payer code (missing 52%) Integer identifier corresponding to 23 distinct values, for example, Blue Cross/Blue Shield, Medicare, and self-pay Medical
12. Medical specialty (missing 53%) Integer identifier of a specialty of the admitting physician, corresponding to 84 distinct values, for example, cardiology, internal medicine, family/general practice, and surgeon
13. Number of lab procedures Number of lab tests performed during the encounter
14. Number of procedures Numeric Number of procedures (other than lab tests) performed during the encounter
15. Number of medications Number of distinct generic names administered during the encounter
16. Number of outpatient visits Number of outpatient visits of the patient in the year preceding the encounter
17. Number of emergency visits Number of emergency visits of the patient in the year preceding the encounter
18. Number of inpatient visits Number of inpatient visits of the patient in the year preceding the encounter
19. Diagnosis 1 The primary diagnosis (coded as first three digits of ICD9); 848 distinct values
20. Diagnosis 2 Secondary diagnosis (coded as first three digits of ICD9); 923 distinct values
21. Diagnosis 3 Additional secondary diagnosis (coded as first three digits of ICD9); 954 distinct values
22. Number of diagnoses Number of diagnoses entered to the system 0%
23. Glucose serum test result Indicates the range of the result or if the test was not taken. Values: “>200,” “>300,” “normal,” and “none” if not measured
24. A1c test result Indicates the range of the result or if the test was not taken. Values: “>8” if the result was greater than 8%, “>7” if the result was greater than 7% but less than 8%, “normal” if the result was less than 7%, and “none” if not measured. (An A1C test is a blood test that reflects your average blood glucose levels over the past 3 months. The A1C test is sometimes called the hemoglobin A1C, HbA1c, glycated hemoglobin, or glycohemoglobin test.)
25. Change of medications Indicates if there was a change in diabetic medications (either dosage or generic name). Values: “change” and “no change”.
26. Diabetes medications Indicates if there was any diabetic medication prescribed. Values: “yes” and “no”.
27. 24 features for medications For the generic names (Label): metformin, repaglinide, nateglinide, chlorpropamide, glimepiride, acetohexamide, glipizide, glyburide, tolbutamide, pioglitazone, rosiglitazone, acarbose, miglitol, troglitazone, tolazamide, examide, sitagliptin, insulin, glyburide-metformin, glipizide-metformin, glimepiride- pioglitazone, metformin-rosiglitazone, and metformin- pioglitazone, the feature indicates whether the drug was prescribed or there was a change in the dosage. Values: “up” if the dosage was increased during the encounter, “down” if the dosage was decreased, “steady” if the dosage did not change, and “no” if the drug was not prescribed.
28. Readmitted (Label) Days to inpatient readmission. Values: “<30” if the patient was readmitted in less than 30 days, “>30” if the patient was readmitted in more than 30 days, and “No” for no record of readmission.

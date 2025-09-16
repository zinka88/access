# Access to Care and Clinical Risk Prediction
Repository for All of Us programs to pull the data and run the analysis for "Access to Care Improves EHR Reliability and Clinical Risk Prediction Model Performance"


## Programs

### Pull Data
- **Create EHR Tables**: Pull in ehr data (2016-2023) for all participants that have ehr data and answered the access survey 
- **Query diabtes lab task data**: Use All of Us dataset builder to pull lab data for the diabetes task.
- **Get Program Measurement Data**: Pull in measurement data collected by the All of Us program. 
- **Create Concept ID Map**: Map concept IDs to concept information. (*output:* condition_source_concept_ids_map.csv)
- **Summarize Access Survey**: Get answers from the access survey (*output:* access_byperson.csv)
- **Summarize Survey Data**: Create datasetes for each of the other surveys including the basics survey, overall health, and familiy history and self-reported health survey (*output:* {basics_survey, self_reported_health}_byperson.csv)
- **Save Type 2 Diabetes Dates**: Get dates for type 2 diabetes codes using concept set from the cohort biulder (diabetes_dates.csv).  
- **Pull Reliability Data**: PUll EHR conditions and compare EHR vs self-report data. (*output*: ehr_condition_codes.csv, ehr_conditions_long.csv, self_conditions_long.csv)
- **Full Sample Summary**: Pulls in information on all participants that have demographic infomration for sample comparison (*output*: all_participant_demo.csv)

## Clean Data/Create Features
- **Create Measurement Features**: Read in the "msrs_YYYY.csv" data and create a set of features using the inputs. These are the EHR data. 

## Analyze Data
- **Analysis Sample**: Create sample of people who responded to the access survey and have EHR data. This will be our main sample of people (*output:* analysis_sample.csv)
- **Sample Summary & Descriptives**: Summarize the sample and compare self-report to EHR data by access status
- **Reliability Analysis**: Create summaries for the reliability plots
- **Rehospitalization Model**: Predict rehospitalizations
- **Diabetes Model**: Predict new diabetes cases
- **Maternal Health R**: Predict adverse pregnancy outcomes (training data created by Irene/Ricky)

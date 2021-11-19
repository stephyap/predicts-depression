## Predict Chronic Pain 
To predict chronic among patients admitted to a tertiary academic medical center in Boston, MA, USA using data from MIMIC-III. 

MIMIC-III (‘Medical Information Mart for Intensive Care’) is a large, single-center database comprising information relating to patients admitted to critical care units at a large tertiary care hospital. Data includes vital signs, medications, laboratory measurements, observations and notes charted by care providers, fluid balance, procedure codes, diagnostic codes, imaging reports, hospital length of stay, survival data, and more. The database supports applications including academic and industrial research, quality improvement initiatives, and higher education coursework.

## Overview of the available tables from the MIMIC-III database (https://mimic.mit.edu/docs/iii/tables/)

The following tables are used to define and track patient stays:

* ADMISSIONS: Every unique hospitalization for each patient in the database (defines HADM_ID)
* CALLOUT: Information regarding when a patient was cleared for ICU discharge and when the patient was actually discharged
* ICUSTAYS: Every unique ICU stay in the database (defines ICUSTAY_ID)
* PATIENTS: Every unique patient in the database (defines SUBJECT_ID)
* SERVICES: The clinical service under which a patient is registered
* TRANSFERS: Patient movement from bed to bed within the hospital, including ICU admission and discharge

Each ICUSTAY_ID corresponds to a single HADM_ID and a single SUBJECT_ID. Each HADM_ID corresponds to a single SUBJECT_ID. A single SUBJECT_ID can correspond to multiple HADM_ID (multiple hospitalizations of the same patient), and multiple ICUSTAY_ID (multiple ICU stays either within the same hospitalization, or across multiple hospitalizations, or both).

The following tables contain data collected in the critical care unit:

* CAREGIVERS: Every caregiver who has recorded data in the database (defines CGID)
* CHARTEVENTS: All charted observations for patients
* DATETIMEEVENTS: All recorded observations which are dates, for example time of dialysis or insertion of lines.
* INPUTEVENTS_CV: Intake for patients monitored using the Philips CareVue system while in the ICU
* INPUTEVENTS_MV: Intake for patients monitored using the iMDSoft Metavision system while in the ICU
* NOTEEVENTS: Deidentified notes, including nursing and physician notes, ECG reports, imaging reports, and discharge summaries.
* OUTPUTEVENTS: Output information for patients while in the ICU
* PROCEDUREEVENTS_MV: Patient procedures for the subset of patients who were monitored in the ICU using the iMDSoft MetaVision system.


The following tables contain data collected in the hospital record system:

* CPTEVENTS: Procedures recorded as Current Procedural Terminology (CPT) codes
* DIAGNOSES_ICD: Hospital assigned diagnoses, coded using the International Statistical Classification of Diseases and Related Health Problems (ICD) system
* DRGCODES: Diagnosis Related Groups (DRG), which are used by the hospital for billing purposes.
* LABEVENTS: Laboratory measurements for patients both within the hospital and in out patient clinics
* MICROBIOLOGYEVENTS: Microbiology measurements and sensitivities from the hospital database
* PRESCRIPTIONS: Medications ordered, and not necessarily administered, for a given patient
* PROCEDURES_ICD: Patient procedures, coded using the International Statistical Classification of Diseases and Related Health Problems (ICD) system


The following tables are dictionaries:

* D_CPT: High-level dictionary of Current Procedural Terminology (CPT) codes
* D_ICD_DIAGNOSES: Dictionary of International Statistical Classification of Diseases and Related Health Problems (ICD) codes relating to diagnoses
* D_ICD_PROCEDURES: Dictionary of International Statistical Classification of Diseases and Related Health Problems (ICD) codes relating to procedures
* D_ITEMS: Dictionary of ITEMIDs appearing in the MIMIC database, except those that relate to laboratory tests
* D_LABITEMS: Dictionary of ITEMIDs in the laboratory database that relate to laboratory tests

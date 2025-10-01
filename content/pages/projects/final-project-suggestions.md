---
content_type: page
description: Suggestions for final projects for 6.S897 Machine Learning for Healthcare.
learning_resource_types:
- Projects
ocw_type: CourseSection
parent_title: Projects
parent_type: CourseSection
parent_uid: 8f308296-4b99-c74b-3eca-95954f1f7ea2
title: Final Project Suggestions
uid: fd4248e5-f68f-2233-10cd-dc3d049961b4
---

Students will produce a final project using a health insurance claims database such as IBM MarketScan, Optum, Center for Medicare & Medicaid Services claims data, or state All-Payer Claims Databases.

Below we describe two types of projects, those focused more on answering a specific clinical question and those focused more on developing novel ML methods. That said, we imagine that many projects may involve a bit of each, and that’s OK!

MIMIC Projects
--------------

### Clinical Projects

MIMIC-III provides a wealth of data to tackle a variety of clinical tasks in the ICU. Here are a few examples of potential clinical questions:

*   Identify organ failure
    *   In the ICU, we are concerned about organ failure in the heart, kidney, liver, and lung. What predictors could be useful for organ failure?
    *   We would want an early enough prediction to be productive and sufficient data in the lab tests (e.g. liver enzymes, creatinine and BUN, blood pressure) in earlier data.
*   Effects of interventions
    *   Which interventions should we do and at what time?
    *   Potential interventions include vasopressors, mechanical ventilation, dialysis, and cardiac assist devices.

Below are some examples of research papers that used the MIMIC-III dataset:

*   Che et al, 2018. "{{% resource_link "6c0c3a87-4ea6-4853-adc2-812423010ebb" "Recurrent Neural Networks for Multivariate Time Series with Missing Values" %}}." _Nature Scientific Reports._ 
*   Dernoncourt et al, 2016. "{{% resource_link "8350ffa3-1ac5-4a03-a6fb-0b5b24610f61" "De-Identification of Patient Notes with Recurrent Neural Networks" %}}." _JAMIA_. 
*   Ghassemi et al, 2014. "{{% resource_link "8dbea310-43cb-4b67-ad4b-e3e3a957cd82" "Unfolding Physiological State: Mortality Modelling in Intensive Care Units" %}}." _KDD_. 
*   Boag et al, 2018. "{{% resource_link "0d1437ea-e21f-4a50-9344-430f454ecd12" "Racial Disparities and Mistrust in End of Life Care" %}}." _MLHC_.
*   Johnson et al, 2017. "{{% resource_link "e49f0b7e-5058-46f0-946a-cb0d8ddc49a8" "Reproducibility in Critical Care: A Mortality Prediction Case Study" %}}." _MLHC_. 
*   Schulam et al. 2016. "{{% resource_link "73619918-54c1-42dc-922f-d9cf480adb60" "Integrative Analysis using Coupled Latent Variable Models for Individualizing Prognoses (PDF)" %}}." _JMLR_. 
*   Young et al. 2018. "{{% resource_link "f453c6cc-6e63-48e1-8eb4-bfce4214af2b" "Uncovering the Heterogeneity and Temporal Complexity of Neurodegenerative Diseases with Subtype and Stage Inference" %}}." _Nature Communications_. 

### Machine Learning Methodology

Similar to above, you can also explore how to extend known machine learning methodology given the challenges of clinical data:

*   Clinical natural language processing (NLP)
    *   How can we better extract entities from the clinical notes such as diseases, symptoms, and treatments? We saw in problem set 3 how existing methods can be flawed. Once we do have these entities, how can we identify relations between the extracted clinical concepts?
    *   Can we construct a timeline from the clinical notes? How would these extracted entities relate with the coded events in the patient chart?
*   Time series
    *   How can we better predict a patient’s progression? Challenges could include missing data, unknown alignment of patients, and heterogeneity of conditions.
    *   How can we interpret a patient’s progression? Clinicians may be interested in how a patient progresses through known concepts (e.g. ICD-9 codes) and also what the specific stages of progression might be.

Projects Using IBM MarketScan Data
----------------------------------

Although not publicly available, students were provided access to the IBM MarketScan research database in the 2019 version of the course. These ideas can easily be extended to other research databases such as Optum, Center for Medicare & Medicaid Services claims data, or state All-Payer Claims Databases. Since the MarketScan research database has coverage of a patient’s full longitudinal clinical trajectory, it is a gold mine for research and already thousands of papers have been published using it. Students should expect to access the data including basic demographics, diagnoses, procedures, outpatient prescription orders, laboratory test orders, and enrollment information.

### Clinical Projects

This type of MarketScan project will focus on studying a new clinical question using machine learning and causal inference methods studied in class.

*   Early detection of a medical condition, e.g. rheumatoid arthritis or Sjogren’s syndrome
*   Causal inference of the effect of an intervention
*   Subtyping or clustering to better understand a population, e.g. individuals rehospitalized within 30-days

Below are examples of papers that have explored some of the above questions. We encourage students to use these for inspiration, but to tackle new clinical questions that weren’t already answered in these (e.g., studying a different disease or a different outcome).

*   _Example of Prediction_: Razavian et al., 2015. "{{% resource_link "f33b5a83-3de0-4b87-99ac-f3a2b8decf29" "Population-Level Prediction of Type 2 Diabetes From Claims Data and Analysis of Risk Factors: Big Data." %}}"
*   _Example of Causal inference_: Brat et al., 2018. "{{% resource_link "a0fdf791-8dd7-4467-807d-5193ba812269" "Postsurgical Prescriptions for Opioid Naive Patients and Association With Overdose and Misuse: Retrospective Cohort Study." %}}"
*   _Example of Characterization_: Hripcsak et al., 2016. "{{% resource_link "f1ecc2b7-d3b2-4e49-9c84-c43ba1405bd0" "Characterizing Treatment Pathways at Scale Using the OHDSI Network, PNAS." %}}"
*   _Example of Subtyping_: Doshi-Velez et al., 2014. "{{% resource_link "69b135d1-c0fa-4f84-85f1-0f4c35bd2d1a" "Comorbidity Clusters in Autism Spectrum Disorders: An Electronic Health Record Time-Series Analysis, Pediatrics." %}}"

### Machine Learning Methodology

The projects mentioned here focus on developing new machine learning methods:

*   Develop better deep learning algorithms for claims data.
    *   Example: widening the gap between the deep learning and baseline methods from {{% resource_link "2b7ce9cf-58a7-449f-8fd1-b84ad9353336" "Rajkomar et al., 2018" %}} and {{% resource_link "51906a68-d9a4-4299-bd1e-16b3f47fa977" "Choi et al., 2016 Doctor AI (PDF)" %}}. You could design {{% resource_link "b0ada66b-7622-4e28-9a3f-096f2ad2d674" "new architectures" %}} that are better suited for medical data, unsupervised learning algorithms (see e.g. {{% resource_link "13b802aa-dfbb-41ea-881f-5f3ebe564089" "Choi et al., 2016 Relationships" %}} and {{% resource_link "efa60938-db0a-4945-8672-f85a05cb44d6" "Beam et al., 2018" %}}), etc.
*   Develop synthetic data generation methods that produce realistic data but have provable privacy guarantees (this is a good project for a group with a theoretical computer science bent).
    *   Recent work has been interested in using deep learning for this, e.g. {{% resource_link "9fb23b43-5951-4c18-b099-12505576120f" "Choi et al., 2017" %}} and {{% resource_link "6711269c-afb5-4707-8596-6033808b7d69" "Hyland et al., 2017" %}}. However, there is a natural trade-off between truly capturing the data density (not just being able to reproduce aggregate statistics from synthetic data) and not leaking private information from the training data. How does one formalize this mathematically?
*   Learn models of what a "normal" treatment policy is for a disease (note: it may be sequential).
    *   How do these differ across populations, either geographic or based on patient characteristics? Can you automatically discover different treatment strategies for the same condition? Can you identify patients that are outliers or are receiving abnormal treatment (these may because of fraud, improper treatment, medical errors, etc.)?
*   Develop algorithms for inferring causality (e.g., one condition causes another, or a medication causes a side-effect) from longitudinal claims data, e.g. by using ideas from Granger causality, the recently developed {{% resource_link "46c003cb-8b44-4751-ac09-6314f063f3f0" "entropic causality" %}}, causal Bayesian networks, or {{% resource_link "ce8478f4-1aea-47ef-9af6-29e92d22b0c0" "Hawkes processes (PDF)" %}}.
*   Develop algorithms to identify and explain non-stationarity, e.g. through changepoint detection and interpretable ML algorithms.

Other Datasets
--------------

*   {{% resource_link "3ac3465c-4ad2-4896-b84a-9bf82128584f" "Multiple Myeloma Research Foundation Compass" %}}
*   {{% resource_link "984b3ff6-1024-4ab4-9a30-940a07a525f8" "The Parkinson’s Progression Markers Initiative" %}}
    *   Specific project suggestion: Learning a representation of MRI images that will help with downstream tasks, e.g. classifying healthy, prodromal, early-stage Parkinson’s, vs late-stage Parkinson’s, or time to outcome. Possible methodologies to consider include {{% resource_link "1ff4e2aa-b0dd-4723-ae50-79a26f404205" "3-D CNN" %}}, {{% resource_link "cccff89d-53f1-491d-a953-a7fc2168f26a" "voxel-based logistic regression" %}}, or principal components. Can you interpret what the representation is capturing?
*   {{% resource_link "2d3704ce-d428-4dfc-b8b5-ec9d34fe691e" "eICU" %}}
    *   Same access requirements as MIMIC-III. eICU has clinical ICU data from 200+ hospitals.
*   Chest X-rays
    *   {{% resource_link "5707743e-ed4e-45a0-adbf-6d4ef1c9f0c8" "The MIMIC-CXR Database" %}}
    *   {{% resource_link "0dc37418-44bf-49a9-9a11-834fbcd1a38b" "CheXpert" %}}
    *   {{% resource_link "330a3227-eb6c-4817-b51b-4cba1ba1a6bf" "Open-i service of the National Library of Medicine" %}}
        
*   {{% resource_link "295a3d8e-5184-4aa9-8a65-bd7708db71da" "The Osteoarthritis Initiative" %}}
*   A more extensive {{% resource_link "c97b36ed-de05-4143-afe0-8e1f4b6bff9f" "list of medical datasets" %}}.
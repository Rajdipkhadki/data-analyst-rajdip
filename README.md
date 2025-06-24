# data-analyst-rajdip
# Descriptive Analysis of Course Completion Records
Understanding Cource completion Records in UCW
# Objective
The main objective of this project was to conduct a descriptive analysis of Course completion record at University Canada West.
- Obtaining information from raw academic and operation sources
- Using relevant data transformation methods like profiling, cleaning and enriching in AWS platform.
- Feeding the clean data to AWS to obtain analytical insight
- The detection of quality problems in data, data gaps, and recommendations of the improvement of quality
# Dataset
The dataset consisted of COurse Completion records from UCW, including the following key features:
1. Completion ID : Unique identifier for each completion record
2. Student ID : Student’s unique ID
3. Course ID : Course identifier
4. Completion Status : Status of the course (Completed, In Progress, Not Completed)
5. Completion date : The date the completion status was recorded

The table below are the example of dataset for this Course Completion Record:

<img width="397" alt="image" src="https://github.com/user-attachments/assets/59a4dfb0-2632-4afd-8a7f-79e798d66994" /> 

# Methodology

1. Data Collection and preparation

Tools Used : S3 bucket was used for loading data and for cleaning the dataset AWS Data GlueBrew was used.

This Image shows storing of our dataset in S3 Bucket.

![image](https://github.com/user-attachments/assets/c28d4cc9-ae61-4f52-a2ec-e6b9c12ae86d)

This Image shows different missing and invalid values.

![image](https://github.com/user-attachments/assets/51c7519a-ad10-4cec-8cd3-9dcaf462af2c)

This image shows the use of AWS data gluebrew for cleaning process.

![image](https://github.com/user-attachments/assets/235c7672-05b2-4ebf-8413-ccc2cf04634e)

2. Descriptive Statistics

Completion Status : Calculated the number of completion status that were completed , not completed or in progress.

<img width="207" alt="image" src="https://github.com/user-attachments/assets/282ca1e5-cc4c-47ae-b34b-2017a9b94323" />

Annual Completion : Calculated the total number of completion throughout whole dataset , this was calculated using Athena.

![image](https://github.com/user-attachments/assets/73b267f6-c554-49c8-9c5b-5d7c69889a9b)

3. Data Visualization

For data visualization AWS Data Glue was used as a tool. In this tool we shared Course Completion Record data set to be joined with Course Performance dataset.

<img width="947" alt="image" src="https://github.com/user-attachments/assets/9451bc2b-0c59-49ec-9bd2-972f8cf16082" />

In this project Visual ETL was used for visualization.

<img width="956" alt="image" src="https://github.com/user-attachments/assets/2cec570f-85a1-4797-8cf0-60b583110857" /> 

4. Student segmentation
- Segmented Student based on the frequency and seversity of complaints.

5. Insights and Finding

a. Low Course Completion Rate
- Only 12 out of 50 students (24%) have completed their courses.
- This indicates a high drop-off rate or extended progression time, as the remaining 76% are either In Progress (44%) or Not Completed (32%).
- This is a significant finding that may require further investigation into course difficulty, student engagement, or support services.

b. High Number of Ongoing Enrollments
- 22 students (44%) are currently in progress, which suggests many learners are either in the early or mid-phase of their courses.
- If these students are clustered around recent enrollment periods, we may expect a spike in completions in upcoming months—monitoring this trend can help forecast learning outcomes.

c. Completion Trends Across Time
- Course completions are spread across multiple months, with no single consistent monthly trend.
- June 2024 had the highest number of completions (3 completions), while December 2024 and January 2025 each had 2 completions.
- This pattern suggests completions may align with academic terms, holidays, or course deadlines.

6. Recommendation
- Introduce early-intervention systems to support students showing slow progress or inactivity.

- Redesign course content to include shorter, interactive modules and flexible deadlines.

- Offer completion incentives and academic support during key periods to boost motivation and success rates.

# Tools and Techniques
1. Storage & Data Lake
- Amazon S3 (Simple Storage Service)
 - Used for storing raw, cleaned, curated, and intermediate datasets:

  a. Academic-raw-raj

  b. Academic-cln-raj

  c. Academic-cur-raj

2. Data Transformation & ETL

a. AWS Glue

- Automates the extract, transform, and load (ETL) process.

- Helps catalog metadata and run serverless jobs.

- Supports creation of a central Data Catalogue (Academic-Data Catalogue-raj).

b. AWS Glue Databrew

- A visual tool for data cleaning and transformation.

- Allows data analysts to clean data without writing code.

- Academic-ETL-raj

- Represents the orchestration logic or ETL scripts possibly triggered using AWS Glue or Lambda.

3. Data Querying & Analytics

a. Amazon Athena

- Serverless interactive query service to analyze data stored in S3 using SQL.

- Ideal for querying cleaned and curated datasets for reporting or insights.

4. Data Cataloging

a. AWS Glue Data Catalogue

- Central metadata repository that makes data in S3 queryable by services like Athena.

5. Data Access & Sharing

a. Internet Access for Teams

- The Academic Data Team accesses the raw and processed datasets through secure internet channels.

- The processed results are available to the Academic-DAP-raj team. 

<img width="799" alt="image" src="https://github.com/user-attachments/assets/7a6cf724-6a2e-4cbf-aae5-2eff7d6dd040" />














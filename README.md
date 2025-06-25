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

# Deliverables
The Academic Data Analysis project delivers a comprehensive set of outputs designed to provide clear insights and enable effective decision-making. The primary deliverable is a detailed descriptive analytics report summarizing patterns in student course completion. This report includes key metrics such as completion rates, monthly completion trends, and a breakdown of completion statuses. In support of this, a data visualization dashboard is created to visually communicate the findings using bar charts, line graphs, and pie charts—tools like Excel, Power BI, or Amazon QuickSight can be used for this purpose.

From a technical perspective, the project includes the full deployment of an ETL (Extract, Transform, Load) pipeline using AWS Glue and Glue Databrew. This pipeline automates the cleaning and transformation of raw course data stored in Amazon S3 buckets (e.g., Academic-raw-raj) and curates it into a structured format within the Academic-cur-raj bucket. The system leverages the AWS Glue Data Catalogue to manage metadata and ensures data is query-ready using Amazon Athena, allowing the academic team to perform real-time SQL-based analytics.

Additionally, a functioning AWS data lake architecture is deployed and documented, showcasing the full flow from raw data ingestion to cleaned and analyzed output. To communicate project results and support strategic planning, a stakeholder presentation is also prepared, summarizing the analytical findings, architectural overview, and actionable recommendations based on student data trends.

# AWS Deployment and Service Models 

![image](https://github.com/user-attachments/assets/570fb5c1-083e-4365-b52b-8a2c9735b6b9)

![image](https://github.com/user-attachments/assets/695eee8b-11b1-4eba-8122-73dd85ec621b)

![image](https://github.com/user-attachments/assets/7bf67466-5c78-4cb7-85b5-e6471a5f87f6)

![image](https://github.com/user-attachments/assets/36bb11c2-831c-4619-8d6b-9be5492ef239)

![image](https://github.com/user-attachments/assets/3fb60312-cb26-4019-81d7-ebdbeff5e408)

#AWS Cost Analysis 

![image](https://github.com/user-attachments/assets/1b62b8ab-ce0d-4735-8f56-58ef94bed11f)


#AWS Global infrastructure 

![image](https://github.com/user-attachments/assets/2aeed90c-f81c-4baa-ae1f-35e2c2fe1f05)

# AWS IAM 
This knowledge has been taken from Module 4 case study.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/ce3306f4-3676-4bfa-b658-f8dd7616419b" />


# AWS VPC
It was easy to navigate through everything but still had error with results.

![image](https://github.com/user-attachments/assets/d2110dd6-7fea-46b1-af23-bdcfacd6979e)


# AWS Lambda 
I tried all the steps but i couldnt get full score.
![image](https://github.com/user-attachments/assets/0604e1e2-ba90-4cc4-aa49-f6538e86b55b)


# AWS EBS 

I tried all the steps written in module but it didnt work.

<img width="571" alt="image" src="https://github.com/user-attachments/assets/89f8d3ca-7b29-4c47-a8ad-4b3861edf43a" />

<img width="549" alt="image" src="https://github.com/user-attachments/assets/331af017-8752-40b8-b4ce-0cdfa50ce3e8" />

<img width="539" alt="image" src="https://github.com/user-attachments/assets/b3d25b47-6dc0-4680-bb4d-0be716de0090" />

# Module 1 knowledge check

<img width="518" alt="image" src="https://github.com/user-attachments/assets/8c2d375d-6107-416f-8d83-b487c906bc2d" />

# Module 2

<img width="522" alt="image" src="https://github.com/user-attachments/assets/92f824a8-a7f7-4912-af73-eb3f74dbae4c" />

# Module 3

<img width="346" alt="image" src="https://github.com/user-attachments/assets/c71d2295-3b7f-480e-9097-f3db464f9a1d" />

# Module 4

<img width="404" alt="image" src="https://github.com/user-attachments/assets/7fad0353-274e-4485-b2e1-5e5feb482267" />

# Module 5

<img width="579" alt="image" src="https://github.com/user-attachments/assets/7dbebe5f-ca41-4bd4-a118-b7e1a8cf9e20" />

# Module 6

<img width="461" alt="image" src="https://github.com/user-attachments/assets/44cdf1f9-b21a-47c6-aeec-805ed4290709" />

# Module 7

<img width="521" alt="image" src="https://github.com/user-attachments/assets/e2084d1b-95ee-486e-a0a4-f477dd1d9019" />



















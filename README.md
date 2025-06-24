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

# Descriptive Statistics

Completion Status : Calculated the number of completion status that were completed , not completed or in progress.

<img width="207" alt="image" src="https://github.com/user-attachments/assets/282ca1e5-cc4c-47ae-b34b-2017a9b94323" />






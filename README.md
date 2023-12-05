#### *Capstone Project: September 2023*

![image](https://github.com/jvenncpe/Feature-Engineering-PostgreSQL/assets/35190918/e2904409-8a97-479a-8ec1-4b8f9861135e)


# Property Sales - Feature Engineering (PostgreSQL)

Capstone project output from "SP701 SQL for Data Engineering" facilitated by Project SPARTA from Development Academy of the Philippines. The course aims to teach us about tidying up and altering data using SQL, shifting data from one database style to another (such as turning operational data into reports) using SQL, and managing large amounts of data in batches using SQL.

## Activity
Perform the following Feature Engineering tasks:
	Task1: Perform One-Hot Encoding on the variable on one or more Categorical Variables in the dataset
	Export: feature_engineering_task1.txt

	Task2: Perform Ordinal or Label encoding on one or more Categorical Variables in the dataset
	Export: feature_engineering _task2.txt

	Task3: Perform Mean encoding on one or more Categorical Variables in the dataset (hint: you may want to use OVER() and PARTITION() commands)
	Export: feature_engineering _task3.txt

	Task4: Perform Mean Normalization on all the numeric variables to rescale these variables (you may add new columns for this)
	Export: feature_engineering _task4.txt

	Task5: Perform Standardization on all the numeric variables to rescale these variables (you may add new columns for this)
	Export: feature_engineering _task5.txt

## Dataset Context

I used data from a food industry company, which includes various Excel files as follows:

![image]

- The first dataset contains invoice details with columns: "Order ID," "Date," "Meal ID," "Company ID," "Date of Meal," "Participants," "Meal Price," and "Type of Meal."
- The second dataset, named "Order Leads," consists of columns such as "Order ID," "Company ID," "Company Name," "Date," "Order Value," and "Converted."
- The third dataset, named "Sales Team," comprises columns like "Sales Rep," "Sales Rep ID," "Company Name," and "Company ID."

These datasets will be utilized to assess sales performance by year, segment customers, and categorize sales team members based on performance, distinguishing between top and bottom performers.

## Methodology
The sales performance analysis was carried out by creating pivot tables and measuring columns in the following steps:
- A pivot table was generated from OrderLeands.xlsx, featuring columns: "Year," "Not Converted," and "Count of Company Id."
- This pivot table data was then used to create another table containing columns: "Year," "Not Converted," "Count of Company Id," "Converted," "Conversion Rate," and "YTY." The "Converted" column was calculated by subtracting the "Count of Company Id" from the "Not Converted" values.
- To calculate the conversion rate, we compared the converted values of the current year with the previous year, minus 1, to ascertain the percentage increase or decrease. The "YTY" column represents the yearly change in the conversion rate.


For RFM Segmentation, the process included creating multiple pivot tables and interconnecting them using "index-match syntax" in the following manner:
- Generated a pivot table from Invoices.xlsx containing "Company ID, Count of Order Id, Max of Order Date, Average of Meal Price," in a new tab for RFM Segmentation Analysis.
- We then added a Sales Representative Column beside the RFM segmentation column by using "index-match" to refer to SalesTeam.xlsx, matching each customer with their assigned sales rep for further sales analysis.
- From the pivot table made using 'index-match' for sales reps, we made a new pivot table to help us sort sales reps by 'Sales Rep Name,' 'At Risk/Need Attrition,' 'Immediate Attention,' 'Loyal Customers,' 'Top Customers,' and 'Grand Total' to analyze their performance.
- By utilizing the newly extracted pivot table, we conduct Sales Representative Segmentation to identifying top and bottom performers based on this information.

This structured methodology enables detailed examination of sales metrics and effective segmentation of sales representatives to pinpoint top and underperforming individuals.

## Results and Discussion

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/03ec8e0d-019c-45e7-9d61-abdebc8351cc)

# Thank you!

---
---
---

# Capstone Peer Grade
## Activity

![Activity](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/b4d850c6-bce1-4906-aef8-dc9ef578022a)



## Criteria

![Criteria](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/43fc56bc-267b-48d1-ad3d-1d432bf4df00)



## Peer Assessment

![1](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f122707d-6ab4-4c9e-9f0a-0664127ba825)


![2](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/1c4ef5d8-881a-4f1c-8091-690c0302cfaa)


![3](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/0ac5ba92-95b5-4d1f-8775-ed01761fe1a2)


![4](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/514b7890-57df-4032-922d-11bdfaa08c37)


![5](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/9e481e81-1142-469f-8d6c-027de05a092e)



## Overall Peer Grade Assessment

![Grade](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/0ca95ba9-c26b-49ff-b897-bf32d93b9fed)


#### *Capstone Project: September 2023*

![image](https://github.com/jvenncpe/Feature-Engineering-PostgreSQL/assets/35190918/e2904409-8a97-479a-8ec1-4b8f9861135e)


# Feature Engineering (PostgreSQL): Property Sales

Capstone project output from "SP701 SQL for Data Engineering" facilitated by Project SPARTA from Development Academy of the Philippines. The course aims to teach us about tidying up and altering data using SQL, shifting data from one database style to another (such as turning operational data into reports) using SQL, and managing large amounts of data in batches using SQL.

## Activity

![Activity](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/4c7983ea-c283-410d-9a5c-82867fc7f462)

## Dataset Context

The dataset describes the sale of individual residential property in Ames, Iowa from 2006 to 2010. The data set contains 2930 observations and originally has a large number of explanatory variables (23 nominal, 23 ordinal, 14 discrete, and 20 continuous) involved in assessing home values.

## Criteria

![Criteria](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/4961daac-6770-4fd9-af9f-cc34d52c4d5b)

## Peer Grade Assessment

![1](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f122707d-6ab4-4c9e-9f0a-0664127ba825)


![2](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/1c4ef5d8-881a-4f1c-8091-690c0302cfaa)


![3](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/0ac5ba92-95b5-4d1f-8775-ed01761fe1a2)


![4](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/514b7890-57df-4032-922d-11bdfaa08c37)


![5](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/9e481e81-1142-469f-8d6c-027de05a092e)



## Overall Peer Grade Assessment

![Grade](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/0ca95ba9-c26b-49ff-b897-bf32d93b9fed)

---

## Methodology
- Identify columns to be used for Feature Engineering techniques like one-hot encoding, nominal or label encoding, mean encoding, mean normalization, or standardization.
- Utilize nested SELECT-QUERY to satisfy the required transformations while handling 'NA' or 'NULL' values within columns like 'lotfrontage'. These values are addressed without removing entire rows; instead, a subquery is employed to transform specific columns, maintaining data integrity by using nested subqueries and conditional transformations.
- After finalizing the SELECT-QUERY, new columns are added to the table to store the transformed data. The SELECT-QUERY is then nested within an INSERT INTO statement to update the tables accordingly.

## Results & Discussion
### Task1: Perform One-Hot Encoding on the variable on one or more Categorical Variables in the dataset
- One-Hot Encoding Output 

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/fd3b9719-86a2-481a-822d-c9a5891a6938)
> Steps Below:
---

- Determine categorical variables and no. of ditinct values to be used for One-Hot Encoding such as below:

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f01ca7ac-cae6-45bc-ab61-59d3302a3e50)

- CATEGORICAL COLUMNS TO USE: lotshape, landcontour, landslope

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/8f6e21e9-bdf1-443e-872e-e3e90714341f)

- Executing a SELECT-FROM query to perform one-hot encoding.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/77add8ea-9c31-4bc9-839e-7f9cae054e64)

- Update table by adding columns for one-hot encoding storage.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/78c2d929-071e-4f84-8029-0d070296d049)

- Populate the added columns from the select query that was used to perform one-hot encoding.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/0a86fd7a-39b5-4cac-a4cf-97a053a7b7a3)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/d90cdb77-967b-4496-a454-78665c423a7b)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/dee55179-bf10-4467-8003-1869deb636c0)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/49b077b3-d278-4fff-a468-c09cfa647012)

- Confirm and validate the values in the added columns

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/d0f93efa-b514-4b80-9c71-781d8a585a3d)

- Display all values

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/356e5d51-f931-46b0-bc21-48e026501ca1)



---
### Task2: Perform Ordinal or Label encoding on one or more Categorical Variables in the dataset

- Ordinal or Label Encoding Output 

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/157972e6-0460-41e9-b76e-49cee1e30d0c)
> Steps Below:
---

- Determine categorical variables and no. of ditinct values to be used for Ordinal or Label Encoding such as below:

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/a7a41739-6207-4420-9772-a33c5a8893e2)

- CATEGORICAL COLUMNS TO USE: overallqual and overallcond

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/21b16c1f-74c1-49c5-be0b-4d5e7d26c0ac)

- Executing a SELECT-FROM query to perform ordinal or label encoding.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/ddb24d36-f33c-4257-8dfe-7e8db8a28554)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/29cd7f14-4bb1-479a-9dd6-e0b1188998c4)

- Update table by adding columns for ordinal or label encoding storage.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/cbad12ed-d04c-4ed9-aa6b-098f6bb7c7d0)

- Populate the added columns from the select query that was used to perform ordinal or label encoding.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/ec9b4dd0-3e7a-473c-b261-438d82735dc6)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/9c100a03-4026-4339-a2fc-7a5dcbc2ceed)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/6e117a0e-3e12-4401-bd57-a23ec8bf4b8c)

- Confirm and validate the values in the added columns, then display all values

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/423c373a-6a47-4758-a5dd-06eba66660c0)

---
### Task3: Perform Mean encoding on one or more Categorical Variables in the dataset
- Mean Encoding Output 

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/8a396e34-7b23-4cea-8a59-d902defb10e8)
> Steps Below:
---

- Determine categorical variables for Mean encoding and Target Variable to Predict/Analyze

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f29b2b22-dc6d-4d22-a8e8-7bbadc7dbed7)

- CATEGORICAL COLUMN TO USE: mssubclass, bldgtype and housestyle
- CHOSEN TARGET VARIABLE: saleprice

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/e28e5895-a1b3-4a1c-8220-0452e2352230)

- Executing a SELECT-FROM query to perform MEAN encoding.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/ea1a8c16-50f5-4078-8b01-cc9b5daa5495)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/fb93edae-3871-4e35-8e76-00f534dea773)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/375b753a-ee2e-4421-806f-d242bb9f50c9)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/93fac566-c5ad-4d57-8e14-ad5a2cc5607d)

- Update table by adding columns for MEAN encoding storage.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/4cf69b55-70f8-4619-b96d-52221cce948c)

- Populate the added columns from the select query that was used to perform MEAN encoding.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/96bf1dae-c5c3-42a2-92a4-740e86071eac)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/281c2dd1-635c-4ccf-9242-40568622dc85)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/0366629a-b51a-4524-a860-ba1f10237aef)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/727bc298-fa10-49f2-82f4-1f4b9b42b5cf)


- Confirm and validate the values in the added columns, then display all values

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/33c15399-de70-40a5-bd3e-a6d885325ef2)

---
### Task4: Perform Mean Normalization on all the numeric variables to rescale these variables 
- Mean Normalization Output 

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f73b97db-1a78-4d11-b16b-3da3129daf2d)

> Steps Below:
---

- Determine numeric variables for Mean Normalization
- NUMERIC COLUMN TO USE: lotfrontage, lotarea, garagearea, grlivarea, totalbsmtsf, saleprice

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/7e29d5b6-724b-435a-aa99-bf53208aaf34)


- Executing a SELECT-FROM query to perform Mean Normalization.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/a6c5c906-79c3-4b3b-9d08-454d2159fc5b)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/a2a6a30b-3865-484b-ab88-4d6e9d59a38b)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/83435d59-b1e0-4aed-9bdb-17a0782d583f)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/b7c2f96f-b782-4d73-9781-585fd79cbdd2)

- To verify rescaling from -1 to 1

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/4b996e50-68ca-4b9e-92b7-bb75bf512696)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/778d959c-addd-443b-a3fb-93ae4835de44)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/14cef5be-2a5f-4b07-b5b5-a67118104fe1)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/2c4ce487-0e16-47d0-8ce8-b86c1758a605)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/6b3931c8-3ee5-4937-b3fe-0e7200e04b82)


- Update table by adding columns for Mean Normalization storage.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f1a2b99d-004c-47e3-b706-15f3d96d5539)


- Populate the added columns from the select query that was used to perform MEAN encoding.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f9a4d34b-b686-4137-8b80-9a8c546c3797)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f65cdeed-2102-465b-abbb-1e197c6fb55b)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/1f9ef5d2-4f24-434c-a62d-2c8dc7d03389)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/3b39c567-4b59-4835-9451-edcfb9a871ff)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/7372539b-8b65-4989-af59-c6e028cff293)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/edb5ba2f-2fee-4a83-a6ef-9723009cf7d3)


- Confirm and validate the values in the added columns, then display all values

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/20a0a77a-fb7d-44eb-acba-56f7b18b9ba0)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f1706ebd-a2ea-443b-8dbd-718b8ff5da86)

---
### Task5: Perform Standardization on all the numeric variables to rescale these variables
- Standardization Output 

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/93674d22-5436-40ef-a38c-0dadbc30a6e7)


> Steps Below:
---

- Determine numeric variables for Standardization
- NUMERIC COLUMN TO USE: garagearea, grlivarea, totalbsmtsf, saleprice

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/1c1c7aaf-78ee-4bd5-a3ee-cee9b18770c0)


- Executing a SELECT-FROM query to perform Standardization.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/2f84bf64-0683-4380-a24b-07aaaf188344)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/c7471e31-72b1-417f-ae89-ebf9e7de6768)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/aa6a6c0b-3f18-4c06-a16a-b70b5286cc89)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/9fc8efd6-7273-4c4c-9b88-de9793adf24e)


- To verify rescaling values

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/174fecb9-fe57-4d75-b9aa-87179de4e917)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/79b81048-bb9d-4560-9c6d-39eba9a1d228)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/10ffe494-d6ca-4e5f-8232-8ada860610a0)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/07f99d2f-bdf0-496a-99ed-40f14a1cba41)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/143c0784-b554-475d-83be-460644846fa7)



- Update table by adding columns for Standardization storage.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/984df6d8-0f08-4a81-af30-bae640c27d86)



- Populate the added columns from the select query that was used to perform Standardization.

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/84b8ca3f-a40c-417f-8bc7-7ddbdc869a50)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/f3aee9cf-59b8-4c18-bcbb-d6338bedfa1b)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/48da1776-9a42-41b8-8bb1-511949f9881a)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/9e8a72a3-a706-40f6-bf51-6091fbc2173e)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/226864d5-9dd5-46ee-bf84-3103ad0bf615)



- Confirm and validate the values in the added columns, then display all values

![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/8ae68c94-81c2-4825-abd1-2e26355960a0)
![image](https://github.com/jvenncpe/Property-Sales-Feature-Engineering-PostgreSQL/assets/35190918/517d1fd2-8504-4b2a-a750-dda49270198a)


# Thank you!



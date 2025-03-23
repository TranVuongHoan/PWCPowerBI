# Data Preparation Analysis

## Data Examination

In the initial phase of the project, I examined the original data files, which were provided in CSV format. Below is a summary of the fields contained in each dataset:

---

### 1. Call Center Dataset

- **Agent**: Name of the call center agent.
- **Date**: Date of the call.
- **Time**: Time of the call.
- **Topic**: Topic of the call (e.g., *Contract*, *Technical*, *Payment*).
- **Answered (Y/N)**: Whether the call was answered.
- **Resolved**: Whether the issue was resolved.
- **Speed of answer in seconds**: Time taken to answer the call.
- **AvgTalkDuration**: Average duration of the call.
- **Satisfaction rating**: Customer satisfaction rating.

---

### 2. Churn Dataset

- **Customer ID**: Unique identifier for each customer.
- **Gender**: Gender of the customer.
- **Senior Citizen**: Whether the customer is a senior citizen.
- **Partner**: Whether the customer has a partner.
- **Dependents**: Whether the customer has dependents.
- **Tenure**: Number of months the customer has been with the company.
- **Phone Service**: Whether the customer has phone service.
- **Multiple Lines**: Whether the customer has multiple lines.
- **Internet Service**: Type of internet service (e.g., *DSL*, *Fiber optic*).
- **Online Security**: Whether the customer has online security.
- **Online Backup**: Whether the customer has online backup.
- **Device Protection**: Whether the customer has device protection.
- **Tech Support**: Whether the customer has tech support.
- **Streaming TV**: Whether the customer has streaming TV.
- **Streaming Movies**: Whether the customer has streaming movies.
- **Contract**: Type of contract (e.g., *Month-to-month*, *One year*, *Two year*).
- **Paperless Billing**: Whether the customer uses paperless billing.
- **Payment Method**: Payment method used by the customer.
- **Monthly Charges**: Monthly charges for the customer.
- **Total Charges**: Total charges for the customer.
- **Churn**: Whether the customer has churned.

---

### 3. Diversity and Inclusion Dataset (Pharma Group AG Sheet)

- **Employee ID**: Unique identifier for each employee.
- **Gender**: Gender of the employee.
- **Job Level**: Job level of the employee.
- **Promotion in FY20**: Whether the employee was promoted in FY20.
- **FY20 Performance Rating**: Performance rating of the employee in FY20.
- **Age Group**: Age group of the employee.
- **Nationality**: Nationality of the employee.
- **Region Group**: Region group based on nationality.
- **Last Hire Date**: Date of the last hire.
- **Years Since Last Hire**: Number of years since the last hire.

---

### 4. Diversity and Inclusion Dataset (Backing 1 Sheet)

- **RAND**: Random identifier for each employee.
- **Employee ID**: Unique identifier for each employee.
- **Gender**: Gender of the employee (*Male*, *Female*).
- **Grade**: Job grade of the employee (e.g., *Junior Officer*, *Manager*, *Director*).
- **Function**: Department or function of the employee (e.g., *Operations*, *Sales & Market*, *Strategy*).
- **OC_RATE**: Organizational commitment rate.
- **PERFORM**: Performance rating of the employee.
- **Y_GRADE**: Yearly grade or performance level.
- **Age**: Age of the employee.
- **Service**: Years of service.
- **Nationality**: Nationality of the employee.
- **Rank 2**: Rank or position within the organization.

---

## Data Transformation

To prepare the data for efficient analysis, I took the following transformation steps:

1. **Add ID Columns**:  
   Added unique identifier (ID) columns to the datasets to standardize the data and make querying more efficient.

2. **Create Mapping Dictionaries**:  
   Created dictionaries to map IDs to detailed descriptions for agents, customers, and employees, ensuring consistency across the datasets.

3. **Validate Data Consistency**:  
   Cross-referenced the dictionaries with the datasets to identify any discrepancies, such as names that did not match those in the dictionaries. This validation step was crucial for maintaining data integrity.

4. **Correct Misspelled Values**:  
   Corrected any misspelled values in the dictionaries to ensure consistency across all files. This helped prevent potential errors during data replacement that could have led to incorrect insights in future analyses.

5. **Replace Full Names with IDs**:  
   Replaced the full names in the datasets with the corresponding IDs for agents, customers, and employees, standardizing the data for optimal querying.

6. **Save the Updated Data**:  
   Saved the updated data in the respective CSV files, ensuring they were properly prepared and optimized for the next phases of the project.

---

## Data Transformation Tools and Outputs

I automated the data transformation process using a Python script, which is available in the following Jupyter Notebook:  
[CSV Files Preparation: Jupyter Notebook](path_to_notebook.ipynb)

The transformed data files resulting from this process can be found in the following directory:  
[Modified Data Files: Directory](path_to_directory)

---

## Additional Data Cleaning Steps

1. **Handling Missing Values**:  
   - Identified and addressed missing or incomplete data, particularly in fields like `product_detail`, `store_location`, `OC_RATE`, and `PERFORM`.  
   - Converted empty string records to `NULL` values to accurately represent missing data.

2. **Standardizing Formats**:  
   - Ensured consistent formatting for dates, times, and numerical values to facilitate accurate analysis.

3. **Removing Duplicates**:  
   - Identified and removed duplicate records to maintain data integrity.

---

## Data Integration

1. **Combining Data Sources**:  
   - Integrated transaction data with additional datasets such as customer information, employee details, and inventory levels to enrich the analysis.

2. **Ensuring Consistency**:  
   - Verified that all integrated data followed the same format and standards.

---

By following this detailed data preparation process, the datasets are now clean, consistent, and ready for in-depth analysis, ensuring accurate and actionable insights for the business.

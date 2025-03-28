# Data Modelling 

## Star Schema Structure

In this project, I will use a **star schema structure** to organize the data for efficient querying and analysis. The star schema consists of a central fact table connected to multiple dimension tables.

---

### Fact Table: `Employee Performance Fact Table`

- **`employee_id`**: Primary Key (PK) uniquely identifying each employee.
- **`date_id`**: Foreign Key (FK) linking to the `Date` dimension table.
- **`performance_rating`**: Performance rating of the employee.
- **`oc_rate`**: Organizational commitment rate.
- **`service_years`**: Years of service of the employee.

---

### Dimension Tables

#### `Employee Dimension Table`

- **`employee_id`**: Primary Key (PK) uniquely identifying each employee.
- **`gender`**: Gender of the employee (*Male*, *Female*).
- **`grade`**: Job grade of the employee (e.g., *Junior Officer*, *Manager*, *Director*).
- **`function`**: Department or function of the employee (e.g., *Operations*, *Sales & Market*, *Strategy*).
- **`nationality`**: Nationality of the employee.
- **`rank`**: Rank or position within the organization.

#### `Date Dimension Table`

- **`date_id`**: Primary Key (PK) uniquely identifying each date.
- **`date`**: Actual date.
- **`day`**: Day of the month.
- **`day_name`**: Name of the day (e.g., *Monday*).
- **`month`**: Month of the year.
- **`year`**: Year.

---

## Data Preparation Analysis for Diversity and Inclusion Dataset (Backing 1 Sheet)

### Data Examination

In the initial phase of the project, I examined the original data files, which were provided in CSV format. Below is a summary of the fields contained in the dataset:

#### Employee Information

- **`RAND`**: Random identifier for each employee.
- **`Employee ID`**: Unique identifier for each employee.
- **`Gender`**: Gender of the employee (*Male*, *Female*).
- **`Grade`**: Job grade of the employee (e.g., *Junior Officer*, *Manager*, *Director*).
- **`Function`**: Department or function of the employee (e.g., *Operations*, *Sales & Market*, *Strategy*).
- **`OC_RATE`**: Organizational commitment rate.
- **`PERFORM`**: Performance rating of the employee.
- **`Y_GRADE`**: Yearly grade or performance level.
- **`Age`**: Age of the employee.
- **`Service`**: Years of service.
- **`Nationality`**: Nationality of the employee.
- **`Rank 2`**: Rank or position within the organization.

---

### Data Cleaning and Transformation

1. **Handling Missing Values**:  
   - Identify and handle missing values in the dataset. For example, convert empty strings to `NULL` values.

2. **Data Type Conversion**:  
   - Ensure that each field has the correct data type (e.g., converting strings to dates, integers to floats).

3. **Normalization**:  
   - Normalize the data to reduce redundancy and improve data integrity.

4. **Data Validation**:  
   - Validate the data to ensure consistency and accuracy (e.g., checking for valid employee IDs, ensuring performance ratings are within a valid range).

---

### Data Loading

1. **Data Import**:  
   - Import the cleaned and transformed data into the database using SQL commands, ensuring correct mapping to the corresponding columns in the tables.

2. **Data Integrity**:  
   - Enforce data integrity constraints (e.g., primary keys, foreign keys) to maintain the accuracy and consistency of the data.

---

## Entity-Relationship Diagram (ERD)

The **Entity-Relationship Diagram (ERD)** visually represents the star schema structure, showing the relationships between the fact and dimension tables. This diagram helps in understanding the database architecture and the flow of data.

![ERD Diagram](Call Center Modelling.png) 

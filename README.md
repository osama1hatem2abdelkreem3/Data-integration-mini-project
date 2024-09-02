# Data-integration-mini-project
# SSIS Flow Project

This project involves creating an SSIS package to perform specific tasks between two SQL Server instances.

## Project Overview

### Assumptions
- There are two SQL Server instances:
  - **MS_Server1**: Contains the `SD_company` database with filled tables.
  - **MS_Server2**: Contains an empty database called `Temp` (no tables exist).

### Control Flow Tasks
As I worked on the project, I successfully completed the following steps:

1. **Create New Table**:  
   I created a new table named `EMP` in the `Temp` database.

2. **Copy Data**:  
   I copied all rows from the `employee` table in the `SD_company` database (on `MS_Server1`) to the newly created `EMP` table in the `Temp` database (on `MS_Server2`).

3. **Row Count**:  
   I displayed the number of rows moved from the `employee` table to the `EMP` table.

4. **Success/Failure Message**:  
   - I displayed a success message if the copy operation was successful.
   - I showed a failure message if the operation failed.

5. **Backup**:  
   I backed up the new changes that occurred in the `Temp` database.

6.**automate execution**
  the file will be automatickly executed each month 
![Screenshot (23)](https://github.com/user-attachments/assets/3adb6cc5-872c-4db4-9f19-45a4c5136323)
![Screenshot (22)](https://github.com/user-attachments/assets/73ac2527-42cc-4c6c-ad0b-77a2da6ecc85)
![Screenshot (21)](https://github.com/user-attachments/assets/cf504ea2-9a95-41af-add1-0b808dc0f009)
![Screenshot (24)](https://github.com/user-attachments/assets/5eb913bd-6dbe-4770-8853-0c9e258ad266)

### Note
- The scheduling task (executing the project using SSMS at the end of each month at 11:00 PM) was not successfully completed.

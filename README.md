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

### Note
- The scheduling task (executing the project using SSMS at the end of each month at 11:00 PM) was not successfully completed.

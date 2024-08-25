## Project Requirement: SSIS Flow Creation

###  Using SSIS to Build the Below Flow

1. **Assumptions (SSMS):**
   - You have two different SQL Server instances:
     - **MS_Server1**: Contains the `SD_company` database with filled tables.
     - **MS_Server2**: Contains an empty database called `Temp` (no tables exist).

2. **Control Flow Tasks:**
   1. **Create New Table:**
      - Create a new table named `EMP` in the `Temp` database.
   
   2. **Backup:**
      - Backup the new changes that occur in the `Temp` database.

   3. **Copy Data:**
      - Copy all rows from the `employee` table in the `SD_company` database (located on `MS_Server1`) to the newly created `EMP` table in the `Temp` database (located on `MS_Server2`).

   4. **Row Count:**
      - Display the number of rows moved from the `employee` table to the `EMP` table.

   5. **Success/Failure Message:**
      - If the copy operation is successful, display a success message; otherwise, display a failure message.

   6. **Checkpoint:**
      - Use a checkpoint if it exists to ensure the process can resume from the last successful point in case of a failure.

   7. **Scheduled Execution:**
      - Execute the project using SSMS at the end of each month at 11:00 PM.

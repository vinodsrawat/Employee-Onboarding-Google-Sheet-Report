# Employee Onboarding Google Sheet Reort

## Problem Statement

The task is to work on an employee onboarding dataset to clean, format, analyse, and derive actionable insights.


### Steps followed 

- Step 1 : Data Cleaning and Organization
  - Dataset is an google sheet, analyse data if it is enough to solve our problem.
  - Examine & Clean the dataset by removing duplicates, correcting any formatting errors in the dataset.

- Step 2 : Formatting for Clarity and Presentation
  - Apply text & cell formatting (bold, italics, font sizes) to differentiate between headers, subheaders, and data.
  - Utilise conditional formatting to visually indicate the data, such as distinguishing between departments or employee status.

- Step 3 : Data Analysis and Table Creation
  - Formulate an auto-updating table for Active Employees, including essential details and a summary of the total count of active employees.

Formula used:

        =FILTER('Task 2.2'!A2:S,'Task 2.2'!F2:F = "Active")
  
        =COUNTA(D:D)-1

  - Formulate an auto-updating table for Inactive Employees, listing them along with relevant information and summarising the total count.

Formula used:

        =FILTER('Task 2.2'!A2:S,'Task 2.2'!F2:F = "Inactive")

        =COUNTA(D:D)-1

  - Formulate an auto-updating table for To Join Employees, showing their details with a role-wise segmentation.

Formula used:

        =FILTER('Task 2.2'!A2:S,('Task 2.2'!F2:F = "To Join") * ('Task 2.2'!E2:E = "HR"))

        =FILTER('Task 2.2'!A2:S,('Task 2.2'!F2:F = "To Join") * ('Task 2.2'!E2:E = "Tech"))

        =FILTER('Task 2.2'!A2:S,('Task 2.2'!F2:F = "To Join") * ('Task 2.2'!E2:E = "Sales"))

        =FILTER('Task 2.2'!A2:S,('Task 2.2'!F2:F = "To Join") * ('Task 2.2'!E2:E = "Marketing"))

        =COUNTA(D:D)-1

  - Formulate an auto-updating table for Bank Details of Employees showcasing pertinent banking information.

Formula used:

        =QUERY('Task 2.2'!A:S, "SELECT C,F,G,H,I,K,N,O,P,Q,R,S", 1)

The above formula creates a table with the columns required.

Where,

Task 2.2 is sheet name

C,F,G,H,I,K,N,O,P,Q,R,S are the column names

1 indicates that 1st row is header


  - Calculate the Role-wise Total CTC of Active Employees and present this information in a clear and concise table.

Formula used:

        =SUMIFS('Task 2.2'!K:K,'Task 2.2'!F:F,"Active",'Task 2.2'!E:E,"HR")

The above formula calculates the sum of CTC of HR department. Same formula is used for the other departments.

- Step 4 : Additional Analysis
  - Analyse the distribution of employees by department and status. Use pivot tables or charts to visualise this data.
  - Calculate the average CTC across different roles and present this information in a graph.
  - Create an automated dashboard summarising key metrics from the dataset, such as total employees by status, average CTC, and role distributions.

 # Report Snapshot

![MIS](https://github.com/vinodsrawat/Vrinda-Strore-Annual-Excel-Report/assets/161686865/df1be047-e68c-4151-8d86-e15f00694ec8)

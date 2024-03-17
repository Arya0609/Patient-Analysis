# HEALTH-CARE DATA ANALYSIS

### Dashboard Link : https://app.powerbi.com/links/Nt1eerHkY8?ctid=03b7ec4d-37cd-45fc-9485-4b09b26e6726&pbi_source=linkShare
## Overall Objective:
### Project Goals
    1. Track Current status of Patient Waiting List
    2. Analyze Historical Monthly Trend of Waiting List in Inpatient & Outpatient Category
    3. Detailed speciality level & age profile analysis.

### Data Scope
2018 - 2021

### Metrics Required
    1. Average & Median Waiting List
    2. Current Total Waiting List

### Views Required
    1. Summary Page
    2. Detailed Page for Granular analysis.

### Terminologies
    1. Inpatient - Patient got admitted for more than one day.
    2. Day Case - Patient got admitted for 1 day.
    3. Outpatient - A Patient who receives medical treatment without being admitted to a hospital.

### Steps followed
    - Step 1 : Data Collection : Used Folder Data Cannector
        - Combine & Load Data
          Note: Check Column count & column headers are same.
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/e1bc32a5-5a56-4f4f-964b-9e1760ffcfa0)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/6cab0d74-e465-4656-829e-49d88dafa2a4)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/0c0743a1-1339-48b1-9272-44f43856bda9)
   - Step 2 : Data Transformation
    - Check the column quality
    - Transformed date column to date data type
    - Count the rows uploaded and tally the same with the CSV file
    - Append both the Inpatient & Outpatient dataset together so that I have a single dataset.
    - While reviewing, there were 2 differences - firstly, speciality_name column names were different so I have renamed the column, secondly case_type column was missing in Outpatient dataset so I have created a custom column in Outpatient dataset as "Outpatient".
    - Append both of these tables using "Append queries as new" and named the data as "All_Data"
    - Removed Blank rows from the columns
    - Replaced & Trimmed the column values in Time_band column as the column values were captured twice.
    - Close & Apply the data.

![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/2ec38187-5c60-432e-96b1-1ff1fea9baf0)


![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/6b139570-22c3-4834-a104-57e1a2245d19) 

   - Step 3 : Data Modelling : 
    - Created a additional mapping table which maps all the specialities to a certain speciality group as there is a humungous number of specialities it becomes easier to Analyze.
    - Imported Mapping_Speciality CSV to Power BI
    - Promoted Column header using transform data
    - Model the data by creating a relationship between mapping_speciality & All_Data.
    - speciality_name is the common attribute in both the tables.

![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/5b8d1451-9a2d-481f-8c0a-36c056c77005)

![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/c69a6e42-b9ad-49a8-ae28-5cec2378c6e2)

   - Step 4 : Data Visualization :
    - Created a dynamic card using DAX measures for Total Wait List (CY vs PY)
    - Created a donut chart for Case Type Split.
    - Required a column chart for displaying the relationship between Time Band Vs Age profile
    - Need a grid to showcase top 5 specialities.
    - All the above charts should be dynamic to Average / Median wait list as there were couple of outliers user can easily switch between any Metrics.
    - To create a dynamic measure, inserted a blank table with rows average & median and a column as Calc Method, named the table as Calculation Method
    - Create a Slicer using Calc_Method column.
    - Created 2 measure avg_waiting_list and median_waiting_list.
    - Create 1 more measure which will enable the user to interact between the slicer button(Average & Median) and switch between these 2 Metrics. Named the measure as Avg/Median Wait List.
    - Created all the 3 charts.
        - Avg/Median Case Type Split
        - Avg/Meddian Time_band Vs Age profile.
        - A multi - row card to showcase the Avg/Median Top 5 specialities.
    - Created a Monthly Trend - Inpatient vs. Outpatient using line chart.
    - Inserted a slicer for date column & case_type
    - Created an Overall Summary Page uptil now.
    - Inserted a new page named as "Detail"
    - Copy Paste few required elements from Summary page to the detail page and synced the visuals.
    - Insert a matrix for Granular level analysis.
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/9029d848-3194-4d2b-bd89-0de5a0d128d2)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/26612d74-651e-42be-bf41-5d0c5db24f14)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/b44fe045-7670-42e8-8886-ee9e8f2d4c40)

![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/14267ef1-3ea3-45c1-9b61-0cafd15d7146)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/d0fc3876-d839-46b2-afe7-6eec44a465f0)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/b4624ec8-9bbf-44ed-bb7a-5d7d86635658)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/507a77c3-39e0-4824-80a9-17068c75e462)

![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/24f39fe3-ee36-474d-a087-6a69c2ccc1dc)
![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/bcc37d51-dd87-4683-904e-3667ffa959e0)


![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/4f4c8d37-1552-4fb9-a995-52ca90f5466d)


![image](https://github.com/Arya0609/Pizza-Sales-Report/assets/163738283/c14ac5f1-7e58-4bec-ba49-5701e3191dff)

   - Step 5 : Beautifying the visuals using MS-PowerPoint
    - Take Report Snapshot.
    - Paste in a PowerPoint and adjust the page size as per the slide size.
    - Designed Power BI background by inserting shapes.
    - Colored the Layout and Designed the background.
    - Extract both the slide as a PNG file.
    - Apply the images as Canvas background in powerbi.
    - Formatted the charts & visuals.
    - Created an Explicit Title that shows whether the average is selected or Median.
    - Added Interactivity & Navigation.
    - Finally published the file in powerbi service.





    





  












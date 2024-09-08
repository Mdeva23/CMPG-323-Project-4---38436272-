## CMPG 323 Project 4 - User Acceptance Testing Automation

## Overview

This project automates the User Acceptance Testing (UAT) process for the NWU Tech Trends Telemetry Portal using Robotic Process Automation (RPA) with UiPath. The purpose of the automation is to simulate the manual process of testing whether records can be correctly added to the web application. The bot reads test data from an Excel file, inputs the data into the web form, verifies if the record was successfully created, and updates the test results in the Excel file.  

Key Features:  
=>Automated Data Input: The bot reads data from an Excel file and automatically fills out the web form.  
=>Record Verification: The bot verifies if the record was created successfully by checking the web application.  
=>Test Result Logging: It logs test results (Pass/Fail) into the Excel file, based on whether the data was successfully added.  

##Table of Contents  
1. Project Setup  
2. Prerequisites  
4. Installation  
5. How to Run the Bot  
    - Step 1: Prepare Test Data    
    - Step 2: Run the UiPath Bot   
    - Step 3: Verify Results  
5. Project Workflow  
6. Input Data  
7. Form Automation  
8. Verification and Logging  
9. References  

## Project Setup  
Prerequisites  
Before running the project, ensure the following tools are installed and set up:  
    =>UiPath Studio: Download and install the UiPath Community Edition from UiPath.  
    =>Excel Application: The bot reads and writes test data from an Excel file, so ensure Excel is installed.  
    =>NWU Tech Trends Telemetry Portal Access: Ensure access to the web application at this URL: https://techtrendstelemetryportal.azurewebsites.net/.  

## Installation
1. Clone the GitHub Repository  
    - This will download the UiPath project files to your local machine.    
2. Open the UiPath Project:  
    - Launch UiPath Studio and open the project from the folder where you cloned the repository.  
3. Publish to Orchestrator:  
    - If using UiPath Orchestrator for deployment, go to the Project tab in UiPath Studio and click Publish.  

## How to Run the Bot  
Step 1: Prepare Test Data  
    - Ensure your test data is in an Excel file named NWU Tech Trends Data.xlsx. The file should include columns like ClientName, DateOnboarded, and ProjectName.  
Step 2: Run the UiPath Bot  
    -Open UiPath Studio and run the automation process.  
      - The bot will:  
          - Open the NWU Tech Trends Telemetry Portal.  
          - Read the data from the Excel file.  
          - Input the data into the web form.  
          - Verify if the record is created.  
          - Update the Excel file with TRUE or FALSE in the “Test Passed” column.  
          
Step 3: Verify Results  
    - After the bot has finished running, open the Excel file NWU Tech Trends Data.xlsx.  
    - Check the Test Passed column to see if the records were successfully created:  
    - TRUE: Record was successfully added to the web application.  
    - FALSE: Record creation failed or an error occurred.  

## Project Workflow  
-Input Data  
    The bot reads input from an Excel file, NWU Tech Trends Data.xlsx.  
    Each row represents one test case, and the bot uses this data to populate the fields in the web form.  
-Form Automation  
    Browser Automation: The bot opens a browser (e.g., Edge), navigates to the web form, and automatically fills out fields for ClientName, DateOnboarded, etc.  
    Submit Form: After filling in the data, the bot clicks the Submit button to create the record.  
    
-Verification and Logging  
    - After submitting the form, the bot navigates to the results page and verifies whether the record was created successfully by checking the presence of key data elements (e.g., ClientName, 
      DateOnboarded).  
    - Logging Results: The bot logs the test results (Pass/Fail) into the “Test Passed” column of the Excel sheet.  
    - If the record is created, the value TRUE is written to the Excel file. If not, FALSE is recorded.  

## REFERENCES  
Adit Kansara. 2019. Excel Automation with RPA - Excel Application RPA | UiPath. UiPath Blog. https://www.uipath.com/community/rpa-community-blog/excel-automation-application-rpa. Date of access: 06 Sep. 2024.  
Automate with Rakesh. 2020. How to Use DataRow Argument in Add Data Row | Add Data Row Activity | Add Data Row UiPath Example. How to Use DataRow Argument in Add Data Row | Add Data Row Activity | Add Data Row UiPath Example (youtube.com). Date of Access: 05 Sep. 2024.  
Automate with Rakesh. 2022. How to Clone a Git Repository on UiPath Studio. How to Clone a Git Repository on UiPath Studio (youtube.com). Date of Access: 05 Sep. 2024.  
Boboc, M. s.a. Excel Automation Tutorial - DataTables Automation | UiPath. https://www.uipath.com/learning/video-tutorials/excel-datatables-automation. Date of access: 05 Sep. 2024.  
Changrui Cheng. 2021. How to retrieve the url of a hyperlink on a webpage? - Help. UiPath Community Forum. https://forum.uipath.com/t/how-to-retrieve-the-url-of-a-hyperlink-on-a-webpage/153379/3. Date of access: 05 Sep. 2024.  
Chris Dease. 2021. Looping through links on a website - Help / Studio. UiPath Community Forum. https://forum.uipath.com/t/looping-through-links-on-a-website/316999/3. Date of access: 06 Sep. 2024.  
CMPG323-IT Developments. 2023. 03 October Project 4 Explained. 03 October Project 4 Explained (youtube.com). Date of Access: 01 Sep. 2024.  
CMPG323-IT Developments. 2023. 14 September weekly virtual class Automation Introduction. 14 September weekly virtual class Automation introduction (youtube.com). Date of Access: 01 Sep. 2024.  
David Martinez. 2020. How to correctly loop through an HTML UL element with For Each - Help / Studio. UiPath Community Forum. https://forum.uipath.com/t/how-to-correctly-loop-through-an-html-ul-element-with-for-each/228378. Date of access: 07 Sep. 2024.  
Excel Automation with Studio. 2021. https://www.youtube.com/watch?v=7SrdrREJtcc. Date of access: 04 Sep. 2024.  
Filipe Ferreira. 2017. For each UiElement - Help. UiPath Community Forum. https://forum.uipath.com/t/for-each-uielement/1515/3. Date of access: 06 Sep. 2024.  
GridoWit. 2021. Login or Sign in using UiPath Web recording. Login or Sign in using UiPath Web recording (youtube.com). Date of Access: 05 Sep. 2024.  
Guillermo Cruz. 2019. Add Data Row, there is no row at position 0 - Help. UiPath Community Forum. https://forum.uipath.com/t/add-data-row-there-is-no-row-at-position-0/151163. Date of access: 05 Sep. 2024.   
JaxXult. 2021. Click on item in the drop-down menu - Help / Activities. UiPath Community Forum. https://forum.uipath.com/t/click-on-item-in-the-drop-down-menu/336908. Date of access: 06 Sep. 2024.  
Jensen, A. 2020. How to get Dates and Times from Excel in the right format with UiPath - Full Tutorial. How to get Dates and Times from Excel in the right format with UiPath - Full Tutorial (youtube.com). Date of Access: 05 Sep. 2024.  
Marko Kostic. 2019. How to get all selectors from one web page - Random and other categories. UiPath Community Forum. https://forum.uipath.com/t/how-to-get-all-selectors-from-one-web-page/126074. Date of access: 07 Sep. 2024.  
Muller, J. 2022a. Automation Solutions Using Design Patterns | Community Blog. UiPath Blog. https://www.uipath.com/community/rpa-community-blog/automation-solutions-using-design-patterns. Date of access: 04 Sep. 2024.    
Muller, J. 2022b. Test Driven Development (TDD) - An Approach to Automation | Community Blog. UiPath Blog. https://www.uipath.com/community/rpa-community-blog/understanding-test-driven-development-an-approach-to-automation. Date of access: 07 Sep. 2024.  
Muller, J. 2024. 04A Introduction to Automation, 16 July 2024. https://efundi.nwu.ac.za/access/content/group/4493dc23-83c1-4f78-aaa6-89a19cd28d5f/Slides/04B%20Introduction%20to%20Automation.pptx. Date of Access: 02 Sep. 2024.  
Muller, J. 2024. 04A Introduction to Testing, 16 July 2024. https://efundi.nwu.ac.za/access/content/group/4493dc23-83c1-4f78-aaa6-89a19cd28d5f/Slides/04A%20Introduction%20to%20Testing.pptx. Date of Access: 02 Sep. 2024.  
Muller, J. 2024. CMPG 323 2024 - Project 4 - Project Brief, 2 Sep 2024. https://efundi.nwu.ac.za/access/content/group/4493dc23-83c1-4f78-aaa6-89a19cd28d5f/Projects/Project%204/CMPG%20323%202024%20-%20Project%204%20-%20Project%20Brief-1.docx. Date of Access: 04 Sep. 2024.  
Muller, J. 2024. NWU Tech Trends Data, 29 Aug 2024. https://efundi.nwu.ac.za/access/content/group/4493dc23-83c1-4f78-aaa6-89a19cd28d5f/Projects/Project%204/NWU%20Tech%20Trends%20Data.xlsx. Date of Access: 04 Sep. 2024.  
Nathan Smith. 2021. How to Convert excel to DataTable in UIPath? - Help / Studio. UiPath Community Forum. https://forum.uipath.com/t/how-to-convert-excel-to-datatable-in-uipath/321763. Date of access: 03 Sep. 2024.  
OpenAI. 2024. ChatGPT (Version GPT-4) [Large language model]. https://chat.openai.com.  
RPA. 2023. UiPath RPA - Read Excel data and enter the Data into Web Form || google form automation. UiPath RPA - Read Excel data and enter the Data into Web Form || google form automation (youtube.com). Date of Access: 05 Sep. 2024.  
Rohit Kashyap. 2021. UiPath Best Practices Guidelines | RPA Implementation. SOAIS. https://www.soais.com/rpa-uipath-best-practices-guidelines/. Date of access: 06 Sep. 2024.  
Shaikh, I. 2019. Reading An Excel File In UiPath. C# corner. https://www.c-sharpcorner.com/article/reading-an-excel-file-in-uipath/. Date of access: 06 Sep. 2024.  
UiPath. 2021a. Get Row Item. UiPath Activities. https://docs.uipath.com/activities/docs/get-row-item. Date of access: 06 Sep. 2024.  
UiPath. 2021b. Manage DataTables. UiPath Activities. https://docs.uipath.com/activities/docs/manage-data-tables. Date of access: 06 Sep. 2024.  
UiPath. 2021c. Read from Excel Files. UiPath Activities. https://docs.uipath.com/activities/docs/read-from-excel-files. Date of access: 04 Sep. 2024.  
UiPath. 2021d. UI Automation. UiPath Studio. https://docs.uipath.com/studio/docs/ui-automation. Date of access: 04 Sep. 2024.  
UiPath. 2024. UI Automation. Studio - UI Automation (uipath.com). Date of Access: 02 Sep. 2024.  
UiPath. s.a. Deployment and configuration considerations. UiPath Orchestrator. https://docs.uipath.com/orchestrator/docs/deployment-and-configuration-considerations. Date of access: 04 Sep. 2024.  
UiPath. s.a. Organization modeling in Orchestrator. UiPath Orchestrator. https://docs.uipath.com/orchestrator/docs/organization-modeling-in-orchestrator. Date of access: 04 Sep. 2024.  
Vinnyt1984. 2021. Looping through similar elements from a desktop application screen by clicking each of those elements. List/Count of elements vary each time the screen gets displayed - Help / Studio. UiPath Community Forum. https://forum.uipath.com/t/looping-through-similar-elements-from-a-desktop-application-screen-by-clicking-each-of-those-elements-list-count-of-elements-vary-each-time-the-screen-gets-displayed/352922. Date of access: 04 Sep. 2024.  
What is a UiPath Software Robot? 2021. https://www.youtube.com/watch?v=3R67RGjZoOM. Date of access: 05 Sep. 2024.  

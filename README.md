#CMPG 323 Project 4 - User Acceptance Testing Automation

#Overview

This project automates the User Acceptance Testing (UAT) process for the NWU Tech Trends Telemetry Portal using Robotic Process Automation (RPA) with UiPath. The purpose of the automation is to simulate the manual process of testing whether records can be correctly added to the web application. The bot reads test data from an Excel file, inputs the data into the web form, verifies if the record was successfully created, and updates the test results in the Excel file.

Key Features:
Automated Data Input: The bot reads data from an Excel file and automatically fills out the web form.
Record Verification: The bot verifies if the record was created successfully by checking the web application.
Test Result Logging: It logs test results (Pass/Fail) into the Excel file, based on whether the data was successfully added.

#Table of Contents
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

#Project Setup
Prerequisites
Before running the project, ensure the following tools are installed and set up:

UiPath Studio: Download and install the UiPath Community Edition from UiPath.
Excel Application: The bot reads and writes test data from an Excel file, so ensure Excel is installed.
NWU Tech Trends Telemetry Portal Access: Ensure access to the web application at this URL: https://techtrendstelemetryportal.azurewebsites.net/.

#Installation
1. Clone the GitHub Repository
    - This will download the UiPath project files to your local machine.
2. Open the UiPath Project:
   - Launch UiPath Studio and open the project from the folder where you cloned the repository.
3. Publish to Orchestrator:
   - If using UiPath Orchestrator for deployment, go to the Project tab in UiPath Studio and click Publish.

#How to Run the Bot
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

#Project Workflow
-Input Data
    The bot reads input from an Excel file, NWU Tech Trends Data.xlsx.
    Each row represents one test case, and the bot uses this data to populate the fields in the web form.
-Form Automation
    Browser Automation: The bot opens a browser (e.g., Edge), navigates to the web form, and automatically fills out fields for ClientName, DateOnboarded, etc.
    Submit Form: After filling in the data, the bot clicks the Submit button to create the record.
-Verification and Logging
    - After submitting the form, the bot navigates to the results page and verifies whether the record was created successfully by checking the presence of key data elements (e.g., Name, 
      DateOnboarded).
    - Logging Results: The bot logs the test results (Pass/Fail) into the “Test Passed” column of the Excel sheet.
    - If the record is created, the value TRUE is written to the Excel file. If not, FALSE is recorded.

#REFERENCES

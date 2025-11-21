# da-analyst-project- 

                                                         Leadership Leverage Conference
da analyst project 
Project Overview

This project demonstrates how unstructured Excel data was cleaned, transformed, and visualized using Power BI.
The dataset represents participants from a Power BI Training Program, containing inconsistencies, missing values, and mixed formats.

The goal was to:

Convert raw, unstructured data into a clean, structured format.

Build an interactive Power BI dashboard to analyze participant details and trends.

Share end-to-end data cleaning, transformation, and visualization steps.

📂 Dataset Information

File Name: Unstructured Data - Power BI Training Participants.xlsx
Type: Excel Dataset
Source: Internal Training Records (Simulated)

Contains:

Participant Name

Email ID

City / Location

Qualification

Gender

Course Date / Batch

Feedback or Rating

Issues Found:

Missing and inconsistent entries

Duplicated participant records

Mixed data formats (text/number/date)

Irregular column names and null fields

🧹 Data Cleaning and Transformation Process

Data preparation was performed inside Power BI (Power Query Editor).
Detailed steps below 👇

🔸 Step 1: Import Data

Imported the Excel file into Power BI Desktop.

Navigated to the correct sheet containing participant data.

Checked for headers, removed unnecessary blank rows.

🔸 Step 2: Renaming Columns

Renamed columns to meaningful, standardized names.
Example:
Participant Name → Name
City/Town → City
E-Mail → Email

🔸 Step 3: Removing Duplicates

Used Remove Duplicates option in Power Query.

Duplicates were found mainly in participant names and emails.

🔸 Step 4: Handling Missing Data

Checked for null or blank cells.

Replaced missing values using logical fills:

Missing City values inferred from previous records.

Blank Qualification replaced with "Not Provided".

🔸 Step 5: Data Type Correction

Converted text columns to proper data types:

Course Date → Date

Feedback → Number

Email → Text

🔸 Step 6: Standardizing Text

Applied transformations:

Trimmed spaces, fixed capitalization (e.g., “chennai” → “Chennai”).

Ensured gender values are standardized (M/F only).

🔸 Step 7: Creating Calculated Columns

Added calculated columns such as:

Batch Month = FORMAT([Course Date], "MMM YYYY")

Participant ID = RANKX(ALL('Participants'), [Name],,ASC)

🔸 Step 8: Load Clean Data

Loaded the cleaned table into Power BI Data Model.

📊 Dashboard Development
📍 Objective:

To create an interactive dashboard for training organizers to view participant trends and performance insights.

📊 Dashboard Pages:

Overview Page

Total Participants

Total Cities Represented

Average Feedback Score

Demographics Analysis

City-wise participant distribution

Gender ratio visualization

Course Feedback Insights

Batch-wise average rating

Trend of participant growth over months

🎨 Visualization Elements:

Bar Charts → Participants by City

Pie Charts → Gender Distribution

Line Chart → Monthly Growth Trend

Card Visuals → KPI Metrics (Total Participants, Avg Rating)

Slicers → Filter by City / Month / Gender

🧠 Insights & Learnings

Most participants were from Chennai and Bangalore.

Average feedback rating: 4.2 / 5 across batches.

Increasing trend in enrollments over time.

Some older records lacked email validation.

⚙️ Tools & Technologies
Tool	Purpose
Power BI Desktop	Data cleaning, transformation & dashboard creation
Power Query Editor	Data preparation & standardization


PowerBI-UnstructuredData-Project/
│
├── data/
│   └── Unstructured Data - Power BI Training Participants.xlsx
│
├── dashboard/
│   └── PowerBI_Dashboard.pbix
│
├── images/
│   ├── Dashboard_Overview.png
│   ├── Feedback_Insights.png
│   └── City_Distribution.png
│
└── README.md





Excel	Raw unstructured dataset
DAX	Calculated columns & measures

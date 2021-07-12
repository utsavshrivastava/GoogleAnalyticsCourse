# GoogleAnalyticsCourse
This project forms the part of Capstone project for the [Google Data Analytics Certificate](https://grow.google/dataanalytics/#?modal_active=none) at [Coursera](https://www.coursera.org/).

#### -- Project Status: [Completed]

## Project Intro/Objective
Maximizing the number of annual memberships by converting the casual riders to annual members for a bik-share company in Chicago, Cyclistic.

### Key Stakeholders
* Lily Moreno – Director of Marketing
* Cyclistic Marketing Analytics Team – Responsible for creating marketing strategies.
* Cyclistic Executive Team – Responsible for approving the recommended marketing program.

### Problem Statement
The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling data insights and professional data visualizations.

### Business Use Case
How do annual members and casual riders use Cyclistic bikes differently? 

### Deliverables
1.	A clear statement of the business task 
2.	A description of all data sources used 
3.	Documentation of any cleaning or manipulation of data 
4.	A summary of your analysis 
5.	Supporting visualizations and key findings
6.	Your  top  three  insights  based  on  your  analysis


### Methods Used
* ETL in Python
* Descriptive Analysis in SQL
* Data Visualization in Tableau
* etc.

### Technologies
* Spreadsheets
* Python
* SQL and BigQuery
* Pandas, jupyter notebooks
* Tableau
* etc. 

## Data Analysis Steps

### Prepare
#### Key Points:
* Data was shared through Amazon cloud storage link.
* Data was organized in 32 zipped files, containing:
  - Trip Data from 2013 to May, 2021 in .csv file format.
  - Station Data from 2013 to 2017 in .csv file format.
* Data is split differently for different years; quarterly/bi-yearly or monthly.
* Data is made available by Motivate International Inc. under [license](https://www.divvybikes.com/data-license-agreement)
* Data should be able to provide different types of riders’ behaviors and usage patterns. And this in turn will help us to solve the business use case in discussion.
* Data file problems:
  - File – type for “Divvy_Trips_2019_Q1” and “Divvy_Trips_2019_Q2” missing.
    Solved - Data type is .csv
  - File “Divvy_Stations_2014-Q1Q2” was in .xlsx file format. 
    Solved – File was opened in spreadsheets and exported to .csv format to keep file type consistency.

#### Conclusion:
After the prepare stage, we have 2 master spreadsheets contained compiled information:
* combined_station_data.csv
* combined_trips_data.csv

### Process
#### Key Steps:
* Ensuring Data Integrity
* Cleaning Data
* Transforming Data to be used in Analysis.
* Verifying the cleaned and transformed data
* Documenting the cleaning and manipulation of data

### Analyze
We did preliminary descriptive analysis in SQL, and got a few initial insights in the difference in behavior for casual and member riders. 
#### Sample Queries
```
SELECT  usertype,
        ROUND(AVG(distance/tripduration)*3600,2) AS `Average_Speed_kmph`,
        ROUND(AVG(tripduration)/60,2) AS `Average_Speed_of_Travel_mins`
FROM `bigquery-sandbox-311309.casestudy1.tripdata`
GROUP BY usertype
LIMIT 10
```
|usertype | Average_Speed_kmph | Average_Speed_of_Travel_mins|
|---------|--------------------|-----------------------------|
|casual | 9.93 | 24.73|
|member | 12.18 | 15.99|




1. Clone this repo (for help see this [tutorial](https://help.github.com/articles/cloning-a-repository/)).
2. Raw Data is being kept [here](Repo folder containing raw data) within this repo.

    *If using offline data mention that and how they may obtain the data from the froup)*
    
3. Data processing/transformation scripts are being kept [here](Repo folder containing data processing scripts/notebooks)
4. etc...

*If your project is well underway and setup is fairly complicated (ie. requires installation of many packages) create another "setup.md" file and link to it here*  

5. Follow setup [instructions](Link to file)

## Featured Notebooks/Analysis/Deliverables
* [Notebook/Markdown/Slide Deck Title](link)
* [Notebook/Markdown/Slide DeckTitle](link)
* [Blog Post](link)


## Contributing DSWG Members

**Team Leads (Contacts) : [Full Name](https://github.com/[github handle])(@slackHandle)**

#### Other Members:

|Name     |  Slack Handle   | 
|---------|-----------------|
|[Full Name](https://github.com/[github handle])| @johnDoe        |
|[Full Name](https://github.com/[github handle]) |     @janeDoe    |

## Contact
* If you haven't joined the SF Brigade Slack, [you can do that here](http://c4sf.me/slack).  
* Our slack channel is `#datasci-projectname`
* Feel free to contact team leads with any questions or if you are interested in contributing!
{"mode":"full","isActive":false}
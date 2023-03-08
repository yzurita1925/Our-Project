
# THIS README IS UNDER ACTIVE EDITING AS THE PROJECT PROGRESSES.


## 1. Project Management

### 1.1 Project Overview:
This is a UCF Data Analytics Bootcamp Final Project. The aim of this project is to develop an accurate and reliable regression model for predicting depression rates in a given FIPS code area utilizing various parameters such as health, employment, economics, education, transportation and weather. 

### 1.2 Project Breakdown:
The end-to-end build of this project will have 5 steps:
1) We will select our input data for the model.
2) We will clean our raw data in order for it to be effectively stored and used within the model.
3) We will design and build our database to store this data.
4) We will design and build our machine learning model.
5) We will design and build our visualizations to derive key insights from our analysis.

### 1.3 Team and Collaboration:
Our team consists of 5 members: Chris Cornelius, Ryan Neblett, Ali Manekia, Yessika Zurita and Ben Pietrancosta. Our collaboration can be broken down into 2 main components:
 - Communication -> We primarily used Slack and Zoom. We have a group Slack thread over which topics can be discussed and resolved as they arise. However, we also have scheduled post-class, 15 minute meets on Mondays and Wednesdays to review the status of our various tasks.
 - Documentation -> We're using Github and Google Drive to share documentation. The idea is that materials required to make the model work are stored and organized on Github. For example, we have our input data, our pre-processing JPN, our machine-learning model code and so on. 
For all supplemental documentation such as contact information, roles, task assignments and so on, we use Google Drive.


### 1.4 Timeline:
We have 3 weeks to complete this project. Each week we will be required to meet pre-defined deliverables.  


## 2. Data pre-processing
### 2.1 Data sourcing:
To define a database in which there are multiple tables that can be merged into a single meta-table used for a regression analysis, we must have a common primary key across the aforementioned data sets. We decided to use county FIPS ID (Federal Information Processing Standard) as our common column for joins.
Consequently our data is sourced from government websites that host data, examples include the CDC (Center for Disease Control), the Department of Transportation and the US Bureau of Labor Statistics.

## Development
The team sourced data tables from the primary parameters and began preprocessing them into usable tables. 
The current plan for this project is to clean the tables then run it into some form of ML model or regression. At that point, we will analyse the results to see what direction we need to push the model.

Once the data is at a point that results and correlations can be made, we will visualize the data on tableau and host the project on AWS so it is publically available outside of github.

## Data
The schema is as follows. 
### Sources
The data for this project is being pulled from the following:
    #Links for data sources here

## The Model

## Results

## Conclusions

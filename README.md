
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
### 2.1 Data sourcing overview:
To define a database in which there are multiple tables that can be merged into a single meta-table used for a regression analysis, we must have a common primary key across the aforementioned data sets. We decided to use county FIPS ID (Federal Information Processing Standard) as our common column for joins.
Consequently our data is sourced from government websites that host data, examples include the CDC (Center for Disease Control), the Department of Transportation and the US Bureau of Labor Statistics.

### 2.2 Individual data set pre-processing:

 - Health Data Preprocessing -> Source: https://chronicdata.cdc.gov/500-Cities-Places/PLACES-Local-Data-for-Better-Health-County-Data-20/swc5-untb/explore/query/SELECT%0A%20%20%60year%60%2C%0A%20%20%60stateabbr%60%2C%0A%20%20%60statedesc%60%2C%0A%20%20%60locationname%60%2C%0A%20%20%60datasource%60%2C%0A%20%20%60category%60%2C%0A%20%20%60measure%60%2C%0A%20%20%60data_value_unit%60%2C%0A%20%20%60data_value_type%60%2C%0A%20%20%60data_value%60%2C%0A%20%20%60data_value_footnote_symbol%60%2C%0A%20%20%60data_value_footnote%60%2C%0A%20%20%60low_confidence_limit%60%2C%0A%20%20%60high_confidence_limit%60%2C%0A%20%20%60totalpopulation%60%2C%0A%20%20%60locationid%60%2C%0A%20%20%60categoryid%60%2C%0A%20%20%60measureid%60%2C%0A%20%20%60datavaluetypeid%60%2C%0A%20%20%60short_question_text%60%2C%0A%20%20%60geolocation%60%2C%0A%20%20%60%3A%40computed_region_bxsw_vy29%60%2C%0A%20%20%60%3A%40computed_region_he4y_prf8%60%0AORDER%20BY%20%60statedesc%60%20DESC%20NULL%20LAST/page/filter.
This data provides various health statistics at a FIPS (county) level and is hosted by the Centers for Disease Control and Prevention.  The table includes data for both 2019 and 2020 and has additional information about the various health measures and FIPS geolocation in the table. The preprocessing work focused primarily on breaking the complex table down into several smaller tables that align with the standards of a relational database (minimize duplicative data across tables, establish singular primary keys, etc.) some of the data was also removed.  
The group chose to focus on 2020 for the project and removed 2019 data entirely. In addition, the metrics included both raw numbers and age-adjusted numbers. The group intends to use average age and other age-related factors in the analysis and elected to eliminate the age-adjusted metrics so as to not skew the results. 
The Base_Data_Preprocessed folder in this Github project includes the Jupyter notebook detailing the preprocessing work, as well as the input and output files generated from it. Note the input file was too large to upload in its raw form and was instead zipped.

 - IRS Refund Data Preprocessing -> Source: https://www.irs.gov/statistics/soi-tax-stats-individual-income-tax-statistics-zip-code-data-soi
 The data provided statistics about tax returns filed with the IRS for calendar year 2020.  The data was aggregated at a ZIP code level, which is more granular than the census bureau’s FIPS-level data from the Health section, so the data was preprocessed using a ZIP-to-FIPS lookup table (source: https://www.huduser.gov/portal/datasets/usps_crosswalk.html).  Note that several of the ZIP codes in the IRS data were dummied out (either 0 or 99999) to indicate unincorporated areas of the US that are sparsely populated.  These were not represented in the health data where the target variable exists and so were dropped.
The IRS_Data_Preprocessed folder in this Github project includes the Jupyter notebook detailing the preprocessing work, as well as the input, output, and lookup files used during that process.  Note the input and output files are too large to reside in Github, even when compressed, and are instead being housed in Google Drive.
Zipped input data: https://drive.google.com/file/d/17HMKhdgRNU5yGKHq19cjoxg6uv_Pf79Z/view?usp=share_link
Zipped output table: https://drive.google.com/file/d/167KzQdsd5Jh-hvg8NogsGjKLA-qwYkK1/view?usp=share_link
- Transportation Data Preprocessing -> Source: https://data.bts.gov/Research-and-Statistics/County-Transportation-Profiles/qdmf-cxm3. This data set provides information concerning transportation measures per county. It was filtered down to columns which were deemed relevant to depression. Also, there is no confirmed timeframe for this data, but we are operating under the assumption that it also belongs to 2020.
- Employment Data Preprocessing (Ryan to fill in details)

## 3. Database design and build
### 3.1 Cloud environment:
We'll be hosting the database on an AWS instance (Ryan to fill in details).

### 3.2 Database design:
(Insert DB schema)


## 4. The Model

## 5. Visualization


## Conclusions

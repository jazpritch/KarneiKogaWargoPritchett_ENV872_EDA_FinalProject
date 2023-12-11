Key Factors Driving Load Growth in PJM and ERCOT - Final Project for ENV 872

## Collaborators 

This project was a collaboration for the Environmental Data Analytics (ENV 872) course for the fall of 2023 at Duke University's Nicholas Scool of the Environment. Collaborators include: 

Hanna Karnei
Haru Koga
Jaimie Wargo
Jazmine Pritchett

## Summary 

The U.S. electric grid is a complex web of deregulated and regulated energy markets operating to provide reliable and affordable electricity to its customers. There are seven deregulated markets in the country, known as Independent System Operators (ISOs) or Regional Transmission Organizations (RTOs). Two grid operators – PJM Interconnection and Electric Reliability Council of Texas (ERCOT) – were selected for this analysis to compare and contrast their electricity load patterns and drivers. The reason for choosing PJM and ERCOT was due to their size, geographic reach, and market dynamism. Combined, ERCOT and PJM provide electricity to 90 million customers – almost a third of the U.S. population. PJM is a grid operator that serves 13 states in the Northeast and the District of Columbia, whereas ERCOT predominantly operates in one state – Texas. Both markets saw significant changes in their energy fuel mix and customer size over the past several decades. The structural differences between PJM and ERCOT, together with their large customer base, present an interesting case for comparison. 

The current analysis aims to answer the following questions: 

Has load in ERCOT and PJM increased over time? If so, has it grown at the same rate across the two energy markets?

What are the key social, economic, and energy-related drivers of electricity demand growth in ERCOT and PJM? Are there any differences between the markets? 

This paper will explore how factors such as population size, employment rate, median income, residential electricity bill, and renewables penetration affect load growth. As the U.S. moves toward a net-zero economy, a large share of the transportation, residential, and industrial sectors will be electrified, thus increasing total electricity demand. To better plan for the future needs of the U.S. electric grid, it is critical to examine the historical trends in electricity load and key aspects affecting it. This analysis aims to shed light on the interplay between electricity consumption and socioeconomic characteristics of the ERCOT and PJM customer base to add to the growing body of literature discussing the past, present, and future of electricity demand in the U.S. 

## Keywords

ERCOT, PJM, Load, Electricity, Energy, Texas, RTO, ISO, Market, Economics, Demographics, Growth 

## Database Information 

Metered hourly data which contain the net energy in megawatt-hours:

PJM Load (2010 - 2022) - https://dataminer2.pjm.com/feed/hrl_load_metered/definition

Real-Time LMP (2013 - 2022) - https://dataminer2.pjm.com/feed/reg_zone_prelim_bill/definition

Day-ahead LMP (2010 - 2022) - https://dataminer2.pjm.com/feed/dasr_results/definition

ERCOT Load (2010 - 2022) - https://www.ercot.com/gridinfo/load/load_hist

ERCOT Average Electricity Price (2010-2022)- https://www.eia.gov/totalenergy/data/monthly/pdf/sec9_11.pdf

ERCOT Median Household Income (2010-2022) - https://fred.stlouisfed.org/series/MEHOINUSTXA672N#

Percent Renewables - https://www.eia.gov/electricity/data/state/

Percent Minority - Subtraction of white only percentages from white population totals (U.S. Census)

Population (2010- 2022) - https://www.census.gov/programs-surveys/popest/data/data-sets.html 


## Folder structure, file formats, and naming conventions 

Repository File Structure:

README 

Data
- Metadata
-- 'ERCOT_HOURLY_Load' README File
-- 'ERCOT_Linear_Model_Data' README File
-- 'PJM_Day_Ahead_Code_Appendix.pdf' guide on data column information 
-- 'PJM_Day_Ahead_Dataset' README File
-- 'PJM_Hourly_Metered_Load_Code_Appendix.pdf' guide on data column information
-- 'PJM_Hourly_Metered_Load' README File
-- 'PJM_Real_Time_Code_Appendix.pdf' guide on data column information 
-- 'ERCOT_Electricity_Prices_Guide.pdf' on data column information 
-- 'existcapacity_annual.xlsx' data referred to in 'ERCOT_Linear_Model_Data' README File
-- 'MEHOINUSTXA672N.xls' data referred to in 'ERCOT_Linear_Model_Data' README File
-- 'PJM_Real_Time_Dataset' README File

- Processed
- Raw
-- ERCOT_Source_Data
--- Contains 2010 - 2022 xls/x files of hourly metered load data.
--- Contains ERCOTLinearModelData CSV file for Demographic data of electricity price, median income, percent renewable, percent minority, population, and average load.
-- PJM_Source_Data
--- PJM Metered Hourly Load CSV file data for 2010 - 2022
--- Day-ahead LMP CSV file data (dasr) for 2010 - 2022
--- Real- time LMP CSV file data (rt) for 2013 - 2022

Working Code
- Growth_Drivers_Simple Rmd file of linear regression code 
- Project Report Draft Rmd file of working drafted report
- Tables Rmd, html, and pdf of code and previews of table for report
- Time Series ERCOT html and Rmd of time series analysis for ERCOT and preview 
- Time Series PJM html and Rmd of time series analysis for PJM and preview 

Project Final Report

RTO-ISOs-map JPEG file for final report 


## Metadata

Metadata for each dataset can be found under the 'Metadata' folder. Each MD file is named after the dataset and contains an appendix on further information on the data from the source. 

## Scripts and code

Libraries used to run script and load plots: 

library(tidyverse)
library(here)
library(dplyr)
library(readxl)
library(lubridate)
library(trend)
library(stats)
library(corrplot)
theme_set - used to set theme 
rbind - merged 2010-2022 individual xls and csv files for PJM load data, ERCOT load data, and PJM day-ahead and real-time data. 
\centering - center table captions
\raggededge - left align subsequent text 

Note: Full code examples for plots and tests can be found in 'Working Code' folder.

## Quality assurance/quality control

Report writing and table creation was first conducted in Google Docs to ensure cohesiveness and quality grammar. All code and scripts were tested for error and reviewed by all group members. 



# ERCOT Linear Model dataset


## Summary
This dataset was prepared for Environmental Data Analytics (ENV 872L) project at Duke University, Fall 2023.

The dataset contains electricity price, median income, percent renewable, percent minority, population, and mean load data compiled from various websites into a google sheets document. Data was inserted for 2010-2022 for the ERCOT operator and state of Texas.

## Database Information

Electricity Price- 
Data were collected from the U.S. Energy Information Administartion (EIA) website (https://www.eia.gov/). Searched for 'Electricity Prices' and generated pdf (https://www.eia.gov/totalenergy/data/monthly/pdf/sec9_11.pdf) which can be found in the metadata as 'ERCOT_Electricity_Prices_Guide.pdf'. 


Median Income- 
Data were collected from the Federal Reserve Economic Data (FRED) website (https://fred.stlouisfed.org/). "Texas" was selected from the 'U.S. Regional Data' Menu  (https://fred.stlouisfed.org/series/MEHOINUSTXA672N#) and an Excel file was generated. Numbers can be found in the 'MEHOINUSTXA672N.xls'. 

Percent Renewable-
Data were collected from the U.S. Energy Information Administartion (EIA) website (https://www.eia.gov/). "Historical State Data" was selected from the 'Analysis and Projections' Menu  (https://www.eia.gov/electricity/data/state/) and a pdf was generated for the Net Geeneration 1990-2022 report. Numbers can be viewed at 'existcapacity_annual.xlsx'. 

Percent Minority- 
Data were collected from the United States Census Bureau website (https://www.census.gov/). "Annual Social and Economic Supplements" was selected from the 'Data & Maps' option  (https://www.census.gov/data/datasets/time-series/demo/cps/cps-asec.html) data was then viewed and calculated by subtracting 'white only' percentages from total population and then inputted for each recorded year.

Population-
Data were collected from the United States Census Bureau website (https://www.census.gov/). "Population and Housing Unit Estimates Datasets" was selected from the 'Our Surveys and Programs' option  (https://www.census.gov/programs-surveys/popest/data/data-sets.html) data was then viewed and inputted for each recorded year.

Mean Load-
Data were collected from the U.S. Energy Information Administartion (EIA) website (https://www.eia.gov/). Values can be found under the Texas Electricity Profile  (https://www.eia.gov/electricity/state/texas/)


Numbers were compiled from different sources and then downloaded and uploaded as a CSV file for 2010 - 2022. titled 'ERCOTLinearModelData.csv'.

Data were accessed 2023-12-06.

## Data Content Information

year- Years 2010 - 2022
average_Price_Tot - Combined residential, commercial, and industrial prices
med_income - Median Household Income for Texas
percent_renew - percentage renewables of Texas
percent_minority - percentage of mnorities in Texas
population- total number of people living in Texas

## Additional Information and Support
For more information, please view the README for the repository.
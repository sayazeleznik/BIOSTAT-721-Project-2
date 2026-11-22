# Data Dictionary  

## Project Description  
To conduct exploratory data analysis and examine the associations between various air pollutants taken from the air pollution monitor at the RDU airport, eventually to study the associations between various air pollutants and sickle cell disease in Durham County, North Carolina.  
  
## Data source  
The data came from the EPA monitor at the RDU airport for the years 2018, 2019, and 2020; the years 2018 and 2019 contains data for January - December, while the year 2020 only contains data from January - April.  

## Raw Data  
The original data sets are provided in the `BIOSTAT-721-Project-2` repository as three .csv files: `AQ_2018.csv`, `AQ_2019.csv`, and `AQ_2020.csv`.  

| **Variable** | **Description** | **Units / Format** |
|---|---|---|
| Date | Date of air quality measurement | MM/DD/YYYY |
| Daily Max 8-hour CO Concentration | Maximum 8-hour average CO concentration | numeric |
| units_CO | Measurement units for CO | ppm |
| Daily Mean PM2.5 Concentration | Daily mean fine particulate matter concentration | numeric |
| units_PM | Measurement units for PM2.5 | ug/m3 LC |
| Daily Max 8-hour Ozone Concentration | Maximum 8-hour average O3 concentration | numeric |
| units_O3 | Measurement units for O3 | ppm |  

## Processed Data  
The `csv_clean()` function processes each year's raw data, returning one observation (row) per date.  

| **Variable** | **Description** | **Units / Format** |
|---|---|---|
| date | Date of air quality measurement | R Date (YYYY-MM-DD) |
| CO | Daily maximum 8-hour average CO concentration | numeric |
| units_CO | Measurement units for CO | ppm |
| PM25 | Daily mean PM2.5 concentration | numeric |
| units_PM | Measurement units for PM2.5 | ug/m3 LC |
| O3 | Daily maximum 8-hour average O3 concentration | numeric |
| units_O3 | Measurement units for O3 | ppm or ppb |  

## Derived Variables  
Variables calculated for exploratory data visualizations. 

| **Variable** | **Description** | **Units / Format** |
|---|---|---|
| month | Calendar month extracted from date | Integer (1-12) |
| year | Calendar year extracted from date | Integer (2018-2020) |
| CO_mean | Monthly mean daily CO concentration, pooled over years | ppm |
| O3_mean | Monthly mean daily O3 concentration, pooled over years | ppm or ppb |
| PM25_mean | Monthly mean daily PM2.5 concentration within each year | ug/m3 LC |
| CO_sd / O3_sd | Standard deviation of daily pollutant concentrations | Corresponding pollutant units |
| CO_n / O3_n | Number of non-missing (no NA's) daily measurements | Count |
| CO_lower / CO_upper | Lower and upper 95% confidence interval bounds for CO | ppm |
| O3_lower / O3_upper | Lower and upper 95% confidence interval bounds for O3 | ppm or ppb |  

## Data Processing Notes  
- Date variable updated to R Date format (YYYY-MM-DD).
- Exact duplicate rows are removed.
- Negative pollutant measurements are set to 0.
- Multiple pollutant measurements on the same date are averaged to obtain daily concentrations
- Missing pollutant measurements are retained as NA.
- Ozone concentrations can be converted from ppm to ppb (1 ppm = 1,000 ppb).
- The 2020 data set contains measurements for January - April only (2018 and 2019 contain January - December).

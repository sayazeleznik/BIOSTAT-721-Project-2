# BIOSTAT-721-Project-2

## Project's purpose  
To conduct exploratory data analysis and examine the associations between various air pollutants taken from the air pollution monitor at the RDU airport, eventually to study the associations between various air pollutants and sickle cell disease in Durham County, North Carolina.  
  
## Data source  
The data came from the EPA monitor at the RDU airport for the years 2018, 2019, and 2020; the years 2018 and 2019 contains data for January - December, while the year 2020 only contains data from January - April.  
  
## File structure  
The repository contains the following files:  
- `AQ_2018.csv`, `AQ_2019.csv`, `AQ_2020.csv`: raw daily air quality measurements collected at the RDU airport monitor.  
- `Project 2 Markdown.Rmd`: RMarkdown document containing the data cleaning function, data processing to a cleaned data tibble, summary table function & summary tables, exploratory plots, and interpretation/justifications.  
- `Project-2-Markdown.docx`: final knitted Word report (hiding code).  
- `data_dictionary.md`: document describing the raw, processed, and derived variables used in the project.  
- `README.md`: project overview, data sources, file structure, and instructions for reproducing the analysis.  
  
## How to reproduce  
For this project. I used the version 2.0.0 of the tidyverse package, version 1.2.1 of the dplyr package, version 1.4.0 of the gt package, version 1.9.5 of the lubridate package, and version 4.0.3 of the ggplot2 package. I am also running R version 4.5.1 (2025-06-13 ucrt).   
  
To access the files, clone or download this repository from GitHub, open the `BIOSTAT-721-Project-2` project in RStudio, ensure that the three .csv files and `Project_2.Rmd` are located in the project directory, install/update any packages that are necessary, open `Project_2.Rmd` in RStudio, select "Knit" to generate the Word report.  
  
The analysis will require the raw .csv files to process each year's data using the `csv_clean()` function, then will combine the processed data sets, and generate summary tables and exploratory plots, as well as include interpretations and justifications.  

## Author & Date  
Saya Zeleznik. November 22nd, 2026. 

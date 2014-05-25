Getting_and_cleaning_data_course_project
========================================

Course project of getting and cleaning data class

Source :- https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
Unzip the data into C:\Users\yourname\Documents\
Put run_analysis.R to C:\Users\yourname\Documents\UCI HAR Dataset\
setwd("\UCI HAR Dataset\\")
source("run_analysis.R")
The latter will run the R script, it will read the dataset and write these files:
mergedCleanDataSet.txt -- 7.95 Mb
dataSetWithAverages.txt -- 220 Kb
Use data <- read.table("dataSetWithAverages.txt") to read the latter.

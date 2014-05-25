Source of the original data: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip .

The R file (run_analysis.R) performs the following steps to clean the data:
1. Merge the training and test sets to create one data set. They are:
--> train/X_train.txt with test/X_test.txt -- the result is a data frame of 10299 x 561.
--> train/subject_train.txt with test/subject_test.txt -- the result is a data frame of 10299 x 1.
--> train/y_train.txt with test/y_test.txt -- the result is also a data frame of 10299 x 1.

2. Read the file features.txt and extract only the measurements related to the mean and standard deviation for each measurement.
The result is a data frame of size 10299 x 66.
3. Read activity_labels.txt and apply descriptive activity names to name all the activities in the extracted data set:
walking
walkingupstairs
walkingdownstairs
sitting
standing
laying
4. The script labels the data set with descriptive names. it then merges the 10299x66 data frame containing features with 10299x1 data frames containing activity labels and subject IDs.
The result is saved as mergedCleanDataSet.txt, a 10299x68 data frame such that the first column contains subject IDs, the second column activity names, and the last 66 columns are measurements. Following are the Names of the attributes: 
tbodyacc-mean-x
tbodyacc-mean-y
tbodyacc-mean-z
tbodyacc-std-x
tbodyacc-std-y
tbodyacc-std-z
tgravityacc-mean-x
tgravityacc-mean-y
5. The script creates a second, independent tidy data set that contains the mean of each measurement for each activity and each subject.
The resulting data frame is saved as dataSetWithAverages.txt.
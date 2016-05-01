# GettingAndCleaningDataProject

The purpose of this repo is to hold data from the Coursera Getting and Cleaning Data class project

#Brief Description of the Original Dataset
The original data used for this project were collected from 30 subjects performing various activities.  Data from the subjects movements were collected using a Samsung Galaxy S II smartphone and were published as part of the following study:

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

The original data can be found at the following URL:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

#Brief Description of the Script
For the class project, an R script was written for the purpose of reading in the raw data, combining measurement values with activity descriptions and individual subject identifiers from two separate data sets.  The two data sets are then combined and only those data representing the mean and standard deviation from each measurement are extracted.  The data is then summarized in a new tidy data set reporting an average from each mean and standard deviation  column.
 

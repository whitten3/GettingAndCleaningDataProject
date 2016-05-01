# GettingAndCleaningDataProject
This file lists the R script written to extract, clean and summarize the data files 
for this project.

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

run_analysis<-function(){
 
  require(dplyr)
  require(plyr)
  
  #read feature descriptions into R, read test and train data into R
    features<-read.table("./UCI HAR Dataset/features.txt")
    featuresVec<-as.vector(features$V2)

    Xtest<-read.table("./UCI HAR Dataset/test/X_test.txt", 
                  col.names=featuresVec)
    Xtrain<-read.table("./UCI HAR Dataset/train/X_train.txt", 
                   col.names=featuresVec)

#create subset of mean and std calculations for each data set
    subsetXtrain<-subset(Xtrain,subset= , select=grep(("\\b.mean\\b|.std"), 
                                         names(Xtrain)))
    subsetXtest<-subset(Xtest,subset= , select=grep(("\\b.mean\\b|.std"), 
                                          names(Xtest)))

#read in activity and subject information into R and append each data set
    activityTest<-read.table("./UCI HAR Dataset/test/y_test.txt", 
                             col.names="activity")
    subjectTest<-read.table("./UCI HAR Dataset/test/subject_test.txt", 
                        col.names="subject")

    activityTrain<-read.table("./UCI HAR Dataset/train/y_train.txt", 
                          col.names="activity")
    subjectTrain<-read.table("./UCI HAR Dataset/train/subject_train.txt", 
                         col.names="subject")

    bindTest<-bind_cols(subjectTest, activityTest, subsetXtest)
    bindTrain<-bind_cols(subjectTrain, activityTrain, subsetXtrain)

#create merged Train and Test data set.  From this, create dataset grouped
#by subject and activity with calculated mean of each measument. 
    completeData<-bind_rows(bindTest, bindTrain)

    end<-ddply(completeData, .(subject, activity), numcolwise(mean))
       

}

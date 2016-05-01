##CodeBook
All data for this project was taken from the Human Activity Recognition Smartphones Dataset, v.1.0, and all raw and metadata from this can be found at:https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

and a full description of the dataset can be found at:http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

#Variables In This Dataset
The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ.

These signals were used to estimate variables of the feature vector for each pattern:  
'-XYZ' is used to denote 3-axial signals in the X, Y and Z directions.

tBodyAcc-XYZ  
tGravityAcc-XYZ 
tBodyAccJerk-XYZ  
tBodyGyro-XYZ 
tBodyGyroJerk-XYZ 
tBodyAccMag 
tGravityAccMag  
tBodyAccJerkMag 
tBodyGyroMag  
tBodyGyroJerkMag  
fBodyAcc-XYZ  
fBodyAccJerk-XYZ  
fBodyGyro-XYZ 
fBodyAccMag 
fBodyAccJerkMag 
fBodyGyroMag  
fBodyGyroJerkMag

The set of variables that were estimated from these signals are: 

mean(): Mean value  
std(): Standard deviation 
mad(): Median absolute deviation  
max(): Largest value in array 
min(): Smallest value in array  
sma(): Signal magnitude area  
energy(): Energy measure. Sum of the squares divided by the number of values.   
iqr(): Interquartile range  
entropy(): Signal entropy 
arCoeff(): Autorregresion coefficients with Burg order equal to 4 
correlation(): correlation coefficient between two signals  
maxInds(): index of the frequency component with largest magnitude  
meanFreq(): Weighted average of the frequency components to obtain a mean frequency 
skewness(): skewness of the frequency domain signal   
kurtosis(): kurtosis of the frequency domain signal   
bandsEnergy(): Energy of a frequency interval within the 64 bins of the FFT of each window. 
angle(): Angle between to vectors.  

For the tidy data set only the mean() and the std() variables were extracted and the average of each were summarized for each subject and activity.

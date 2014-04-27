CodeBook
========================================================

## Original dataset 
Final output is a set of transformations applied on [Human Activity Recognition Using Smartphones](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) dataset, which description can be found [here](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)

## Transformations

1. Merge the training and the test sets from the original data set, and adds two columns called "subject_ID" and "activity" which refer to the ID of the person who performed the activity for each measurment and the coded activity respectively.
2. Extracts only the measurements on the mean and standard deviation for each measurement, keeping subject ID and activity columns. 
3. Changes coded activity names (from 1 to 6) to the proper names of each activity.
4. Modify slightly labels on the data set removing any parenthesis and replacing "-" symbol with "_".

A dataset named **"tidyData.txt"** is then saved in the working directory, 10299 observations of 68 variables.

5. Calculates the average of each variable for each activity and each subject. 

A dataset named **"averageData.txt"** is then saved in the working directory, 180 observations of 68 variables.
              
## Variables

*A full description can be found on the [link](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) provided previously but for clarity some of the information has been included in this CodeBook*

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix 't' to denote time) were captured at a constant rate of 50 Hz. Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz. 

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag). 

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (Note the 'f' to indicate frequency domain signals). 

These signals were used to estimate variables of the feature vector for each pattern, from which the script substracts only  the mean *(mean)* and standard deviation *(sdt)*  
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

The complete list of variables of each feature vector is:

- **subject_ID:** *(Factor)* takes values from 1 to 30, number of people involved in the experiment                
- **activity:** *(Factor)* takes values "WALKING", "WALKING_UPSTAIRS", "WALKING_DOWNSTAIRS", "SITTING", "STANDING" AND "LAYING"             
- **tBodyAcc_mean_X:** *(Numeric)*  normalized between -1 and 1      
- **tBodyAcc_mean_Y:** *(Numeric)*  normalized between -1 and 1    
- **tBodyAcc_mean_Z:** *(Numeric)*  normalized between -1 and 1             
- **tBodyAcc_std_X:** *(Numeric)*  normalized between -1 and 1              
- **tBodyAcc_std_Y:** *(Numeric)*  normalized between -1 and 1              
- **tBodyAcc_std_Z:** *(Numeric)*  normalized between -1 and 1             
- **tGravityAcc_mean_X:** *(Numeric)*  normalized between -1 and 1          
- **tGravityAcc_mean_Y:** *(Numeric)*  normalized between -1 and 1          
- **tGravityAcc_mean_Z:** *(Numeric)*  normalized between -1 and 1          
- **tGravityAcc_std_X:** *(Numeric)*  normalized between -1 and 1          
- **tGravityAcc_std_Y:** *(Numeric)*  normalized between -1 and 1           
- **tGravityAcc_std_Z:** *(Numeric)*  normalized between -1 and 1           
- **tBodyAccJerk_mean_X:** *(Numeric)*  normalized between -1 and 1         
- **tBodyAccJerk_mean_Y:** *(Numeric)*  normalized between -1 and 1        
- **tBodyAccJerk_mean_Z:** *(Numeric)*  normalized between -1 and 1         
- **tBodyAccJerk_std_X:** *(Numeric)*  normalized between -1 and 1          
- **tBodyAccJerk_std_Y:** *(Numeric)*  normalized between -1 and 1          
- **tBodyAccJerk_std_Z:** *(Numeric)*  normalized between -1 and 1         
- **tBodyGyro_mean_X:** *(Numeric)*  normalized between -1 and 1            
- **tBodyGyro_mean_Y:** *(Numeric)*  normalized between -1 and 1            
- **tBodyGyro_mean_Z:** *(Numeric)*  normalized between -1 and 1            
- **tBodyGyro_std_X:** *(Numeric)*  normalized between -1 and 1            
- **tBodyGyro_std_Y:** *(Numeric)*  normalized between -1 and 1             
- **tBodyGyro_std_Z:** *(Numeric)*  normalized between -1 and 1             
- **tBodyGyroJerk_mean_X:** *(Numeric)*  normalized between -1 and 1        
- **tBodyGyroJerk_mean_Y:** *(Numeric)*  normalized between -1 and 1       
- **tBodyGyroJerk_mean_Z:** *(Numeric)*  normalized between -1 and 1        
- **tBodyGyroJerk_std_X:** *(Numeric)*  normalized between -1 and 1         
- **tBodyGyroJerk_std_Y:** *(Numeric)*  normalized between -1 and 1         
- **tBodyGyroJerk_std_Z:** *(Numeric)*  normalized between -1 and 1        
- **tBodyAccMag_mean:** *(Numeric)*  normalized between -1 and 1            
- **tBodyAccMag_std:** *(Numeric)*  normalized between -1 and 1             
- **tGravityAccMag_mean:** *(Numeric)*  normalized between -1 and 1         
- **tGravityAccMag_std:** *(Numeric)*  normalized between -1 and 1         
- **tBodyAccJerkMag_mean:** *(Numeric)*  normalized between -1 and 1        
- **tBodyAccJerkMag_std:** *(Numeric)*  normalized between -1 and 1         
- **tBodyGyroMag_mean:** *(Numeric)*  normalized between -1 and 1           
- **tBodyGyroMag_std:** *(Numeric)*  normalized between -1 and 1           
- **tBodyGyroJerkMag_mean:** *(Numeric)*  normalized between -1 and 1       
- **tBodyGyroJerkMag_std:** *(Numeric)*  normalized between -1 and 1        
- **fBodyAcc_mean_X:** *(Numeric)*  normalized between -1 and 1             
- **fBodyAcc_mean_Y:** *(Numeric)*  normalized between -1 and 1            
- **fBodyAcc_mean_Z:** *(Numeric)*  normalized between -1 and 1             
- **fBodyAcc_std_X:** *(Numeric)*  normalized between -1 and 1              
- **fBodyAcc_std_Y:** *(Numeric)*  normalized between -1 and 1              
- **fBodyAcc_std_Z:** *(Numeric)*  normalized between -1 and 1             
- **fBodyAccJerk_mean_X:** *(Numeric)*  normalized between -1 and 1         
- **fBodyAccJerk_mean_Y:** *(Numeric)*  normalized between -1 and 1         
- **fBodyAccJerk_mean_Z:** *(Numeric)*  normalized between -1 and 1         
- **fBodyAccJerk_std_X:** *(Numeric)*  normalized between -1 and 1         
- **fBodyAccJerk_std_Y:** *(Numeric)*  normalized between -1 and 1          
- **fBodyAccJerk_std_Z:** *(Numeric)*  normalized between -1 and 1          
- **fBodyGyro_mean_X:** *(Numeric)*  normalized between -1 and 1            
- **fBodyGyro_mean_Y:** *(Numeric)*  normalized between -1 and 1           
- **fBodyGyro_mean_Z:** *(Numeric)*  normalized between -1 and 1            
- **fBodyGyro_std_X:** *(Numeric)*  normalized between -1 and 1             
- **fBodyGyro_std_Y:** *(Numeric)*  normalized between -1 and 1             
- **fBodyGyro_std_Z:** *(Numeric)*  normalized between -1 and 1            
- **fBodyAccMag_mean:** *(Numeric)*  normalized between -1 and 1           
- **fBodyAccMag_std:** *(Numeric)*  normalized between -1 and 1             
- **fBodyBodyAccJerkMag_mean:** *(Numeric)*  normalized between -1 and 1    
- **fBodyBodyAccJerkMag_std:** *(Numeric)*  normalized between -1 and 1    
- **fBodyBodyGyroMag_mean:** *(Numeric)*  normalized between -1 and 1       
- **fBodyBodyGyroMag_std:** *(Numeric)*  normalized between -1 and 1        
- **fBodyBodyGyroJerkMag_mean:** *(Numeric)*  normalized between -1 and 1   
- **fBodyBodyGyroJerkMag_std:** *(Numeric)*  normalized between -1 and 1   

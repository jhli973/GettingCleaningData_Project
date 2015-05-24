 ## This file provide the detaieled infomation about the variable used in the project

> Variables
* Commonly used variable
  + mean()
         Mean value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         
  + std()
         Standard deviation  
  + meanFreq()
         Weighted average of the frequency components to obtain a mean frequency        

* Variables added to the mergered tidy data
  + activityNo  
          y_test and y_train data  
  + subject_id  
          subject_test and subject_train data                     
  + activityName 
          activity labels merged into the tidy data                   
  + subject_activity  
          a composite column after pasting subject_id with activityName 
  + X
          denote 3-axial signals in the X directions   
  + Y
          denote 3-axial signals in the Y directions  
  + Z
          denote 3-axial signals in the Z directions           

* Variable derived from the data
  + time domain signal for body accelaration mean or standard deviation (std) for x, y and z axials
      tBodyAcc-mean()-X               
      tBodyAcc-mean()-Y               
      tBodyAcc-mean()-Z              
      tBodyAcc-std()-X                
      tBodyAcc-std()-Y                
      tBodyAcc-std()-Z      

 + time domain signal for gravity accelaration mean or standard deviation (std) for x, y and z axials          
     tGravityAcc-mean()-X           
     tGravityAcc-mean()-Y           
     tGravityAcc-mean()-Z           
     tGravityAcc-std()-X             
     tGravityAcc-std()-Y            
     tGravityAcc-std()-Z   Jerk signals

 + time domain signal for Jerk signals mean or standard deviation (std) for x, y and z axials           
    tBodyAccJerk-mean()-X           
    tBodyAccJerk-mean()-Y           
    tBodyAccJerk-mean()-Z          
    tBodyAccJerk-std()-X           
    tBodyAccJerk-std()-Y           
    tBodyAccJerk-std()-Z   

 + time domain signal for gravity accelaration mean or standard deviation (std) for x, y and z axials            
     tBodyGyro-mean()-X             
     tBodyGyro-mean()-Y              
     tBodyGyro-mean()-Z              
     tBodyGyro-std()-X               
     tBodyGyro-std()-Y              
     tBodyGyro-std()-Z   

 + time domain signal for gyroscope Jerk mean or standard deviation (std) for x, y and z axials               
    tBodyGyroJerk-mean()-X          
    tBodyGyroJerk-mean()-Y          
    tBodyGyroJerk-mean()-Z         
    tBodyGyroJerk-std()-X           
    tBodyGyroJerk-std()-Y           
    tBodyGyroJerk-std()-Z    

 + time domain signal for body accelaration magnitude mean or standard deviation (std)            
    tBodyAccMag-mean()             
    tBodyAccMag-std()   

+ time domain signal for gravity accelaration magnitude mean or standard deviation (std)                   
    tGravityAccMag-mean()           
    tGravityAccMag-std()   

+ time domain signal for body accelaration Jerk magnitude mean or standard deviation (std)              
    tBodyAccJerkMag-mean()         
    tBodyAccJerkMag-std()  

+ time domain signal for body gyroscope magnitude mean or standard deviation (std)  
    tBodyGyroMag-mean()             
    tBodyGyroMag-std() 

+ time domain signal for body gyroscope magnitude mean or standard deviation (std)               
    tBodyGyroJerkMag-mean()        
    tBodyGyroJerkMag-std()    frequency domain signals

+ frequency domain signal for body accelaration mean,standard deviation (std), or meanFreq for x, y and z axials      
    fBodyAcc-mean()-X               
    fBodyAcc-mean()-Y               
    fBodyAcc-mean()-Z              
    fBodyAcc-std()-X                
    fBodyAcc-std()-Y                
    fBodyAcc-std()-Z   
    fBodyAcc-meanFreq()-X          
    fBodyAcc-meanFreq()-Y           
    fBodyAcc-meanFreq()-Z 

+ frequency domain signal for body accelaration Jerk standard deviation (std), or meanFreq for x, y and z axials           
    fBodyAccJerk-mean()-X           
    fBodyAccJerk-mean()-Y          
    fBodyAccJerk-mean()-Z           
    fBodyAccJerk-std()-X            
    fBodyAccJerk-std()-Y            
    fBodyAccJerk-std()-Z  
    fBodyAccJerk-meanFreq()-X       
    fBodyAccJerk-meanFreq()-Y       
    fBodyAccJerk-meanFreq()-Z  

+ frequency domain signal for body gyroscope standard deviation (std), or meanFreq for x, y and z axials            
    fBodyGyro-mean()-X             
    fBodyGyro-mean()-Y              
    fBodyGyro-mean()-Z              
    fBodyGyro-std()-X               
    fBodyGyro-std()-Y              
    fBodyGyro-std()-Z  
    fBodyGyro-meanFreq()-X          
    fBodyGyro-meanFreq()-Y          
    fBodyGyro-meanFreq()-Z   

+ frequency domain signal for body accelaration magnitude mean,standard deviation (std) or meanFreq                  
    fBodyAccMag-mean()              
    fBodyAccMag-std()  
    fBodyAccMag-meanFreq() 

+ frequency domain signal for body accelaration Jerk magnitude,standard deviation (std) or meanFreq              
    fBodyBodyAccJerkMag-mean()     
    fBodyBodyAccJerkMag-std()       
    fBodyBodyAccJerkMag-meanFreq()  

+ frequency domain signal for body gyroscope magnitude mean,standard deviation (std) or meanFreq  
    fBodyBodyGyroMag-mean()         
    fBodyBodyGyroMag-std()         
    fBodyBodyGyroMag-meanFreq()  

+ frequency domain signals for body gyroscope Jerk magnitude mean,standard deviation (std) or meanFreq               
    fBodyBodyGyroJerkMag-mean()     
    fBodyBodyGyroJerkMag-std()      
    fBodyBodyGyroJerkMag-meanFreq()


> link for the data
* https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
 
> ZIP files Lists
* ./UCI HAR Dataset/activity_labels.txt                          
* ./UCI HAR Dataset/features.txt                                
* ./UCI HAR Dataset/features_info.txt                            
* ./UCI HAR Dataset/README.txt                                  
* ./UCI HAR Dataset/test/Inertial Signals/body_acc_x_test.txt    
* ./UCI HAR Dataset/test/Inertial Signals/body_acc_y_test.txt   
* ./UCI HAR Dataset/test/Inertial Signals/body_acc_z_test.txt    
* ./UCI HAR Dataset/test/Inertial Signals/body_gyro_x_test.txt  
* ./UCI HAR Dataset/test/Inertial Signals/body_gyro_y_test.txt   
* ./UCI HAR Dataset/test/Inertial Signals/body_gyro_z_test.txt  
* ./UCI HAR Dataset/test/Inertial Signals/total_acc_x_test.txt   
* ./UCI HAR Dataset/test/Inertial Signals/total_acc_y_test.txt  
* ./UCI HAR Dataset/test/Inertial Signals/total_acc_z_test.txt   
* ./UCI HAR Dataset/test/subject_test.txt                       
* ./UCI HAR Dataset/test/X_test.txt                              
* ./UCI HAR Dataset/test/y_test.txt                             
* ./UCI HAR Dataset/train/Inertial Signals/body_acc_x_train.txt  
* ./UCI HAR Dataset/train/Inertial Signals/body_acc_y_train.txt 
* ./UCI HAR Dataset/train/Inertial Signals/body_acc_z_train.txt  
* ./UCI HAR Dataset/train/Inertial Signals/body_gyro_x_train.txt
* ./UCI HAR Dataset/train/Inertial Signals/body_gyro_y_train.txt 
* ./UCI HAR Dataset/train/Inertial Signals/body_gyro_z_train.txt
* ./UCI HAR Dataset/train/Inertial Signals/total_acc_x_train.txt 
* ./UCI HAR Dataset/train/Inertial Signals/total_acc_y_train.txt
* ./UCI HAR Dataset/train/Inertial Signals/total_acc_z_train.txt 
* ./UCI HAR Dataset/train/subject_train.txt                     
* ./UCI HAR Dataset/train/X_train.txt                            
* ./UCI HAR Dataset/train/y_train.txt   
# GettingCleaningData_Project
The project for this course

# Introduction about the how the script function

## To run the script (run_analysis.R), you need to install package "reshape2" and basic R package
install.packages("reshapr2")
library(reshape2)

## 1. download and unzip the data
*download data
url<-"http://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
download.file(url,"run.zip", mode="wb")

*Unzip data
unziprun<-unzip("run.zip")

##Get the information about the data
*read readme file
readme<-readLines(unziprun[4])

*read features_info
features_info<-readLines(unziprun[4])


### 2. Read the data from the unziped files
*read test data
X_test<-read.table(unziprun[15])
subject_test<-read.table(unziprun[14])
Y_test<-read.table(unziprun[16])

*read train data
X_train<-read.table(unziprun[27])
subject_train<-read.table(unziprun[26])
Y_train<-read.table(unziprun[28])

*read features from the unziped file
features<-read.table(unziprun[2])

*read activity from the unziped files
activity<-read.table(unziprun[1])

## 3. Cleanning the data
*name X_test and X_train data
names(X_test)<-as.character(features[,2])
names(X_train)<-as.character(features[,2])

## Extract/Subset the mean and std data, someone sue the first two command which remove meanFreq() data
#X_test_sub<-X_test[, as.vector(grep("(.*)mean\\(\\)(.*)|(.*)std\\(\\)", as.character(features[,2]), value=FALSE))]
#X_train_sub<-X_train[, as.vector(grep("(.*)mean\\(\\)(.*)|(.*)std\\(\\)", as.character(features[,2]), value=FALSE))]

X_test_sub<-X_test[, as.vector(grep("mean|std", as.character(features[,2]), value=FALSE))]
X_train_sub<-X_train[, as.vector(grep("mean|std", as.character(features[,2]), value=FALSE))]

*combine data, subject and test/activity
> X_test_data<-cbind(X_test_sub, subject_test, Y_test)
> X_train_data<-cbind(X_train_sub, subject_train, Y_train)

*add names to the new colummns 80, and 81
names(X_test_data)[80]<-"subject_id"
names(X_test_data)[81]<-"activity"
names(X_train_data)[80]<-"subject_id"
names(X_train_data)[81]<-"activity"

*Merge data
X_test_data_act<-merge(X_test_data, activity, by.x="activity", by.y="V1", all=TRUE)
X_train_data_act<-merge(X_train_data, activity, by.x="activity", by.y="V1", all=TRUE)

*Combine all test and train data
final_data<-rbind(X_test_data_act, X_train_data_act)

*Name the columns 
names(final_data)[1]<-"activityNo"
names(final_data)[82]<-"activityName"

## 4. return the tidy data
final_data

## 5. Summarize the data

*load the package "reshape2"
library(reshape2)

*create a new column by pasting column subject and activityName
final_data$subject_activity<-paste(final_data[,81],final_data[,82])

*melt the data by setting the new column as id and all measure cols as variables
final_data_mel<-melt(final_data, id="subject_activityName", measure.vars=as.vector(names(final_data)[2:80]))

*summarize the data by dcast
sum_data<-dcast(final_data_mel, subject_activity ~ variable, mean)

*return the tidy data as 
sum_data

*Save data in the current directory as "sum_data.txt"
write.table(sum_data, "./sum_data.txt", row.name=FALSE)



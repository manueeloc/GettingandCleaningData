Codebook
#New variables
train_x<- stores the measurments of the device, reads the x_train. txt file and haves as colnames the features file
train_y<- store the activity that the subject is doing have as name "Activity_ID" range 1:6
subject_train<-store the identificacion of the subject as an integer
test_x<- stores the measurments of the device, reads the x_test. txt file and haves as colnames the features file
test_y<- store the activity that the subject is doing have as name "Activity_ID" range 1:6
subject_test<-store the identificacion of the subject as an integer
There is no mayor transformation for this variable so each value is the same as the original file.

#Data transformation
merged_data<-combine the train and the subject data
data_extracted<-in this variable is stored the data with the mean and the standard deviation of the merged data
descriptive_data<- It is added a string column which indicate the activity from which each measure was taken

#Tidy data
Tidydata<- from this variable the measuremente was grouped by the activity and the subject and in each group the average of each measurement (mean and std) and then it was stored



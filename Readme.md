The code works the following way

First it creates a folder "data" where it stores the unzipped files from the wearables data set
Second it stores the pathfile from each of the files in this folder in a vector called Files
Third it creates a group of tables test_x, test_y and subject_test, train_x, train_y, subject_train
test_X contains the measuremnts of the wearable and is named borrowing the names of the feature file in the dataset
test_y contains the activity that the subject was doing and its valure varie from 1 to 6 each of these number represents an activity and it can be seen from the activity label file in the dataset and it is named as "Activity_ID"
and the subject_test it stores the device or person from wich the measurement was taken, and it is named as "Subject_ID"
The same logic is applied for the tables train_x, train_y and subject_train
Then the tables are combined using cbind and rbind

The next part of the code creates a boolean vector where it check if the string "std|mean" appears in the column names of the merged data
then the columns of the merged data is evaluated using the boolean vector extracting in this way the columns where the mean and the standard desviation is evaluated, extracting the measuremnts that matter to us

Then we add the descriptive value of the activity ID, to do this we use the merge function of r and we merge the previous table and we merged with the table where it is stored the label of the activitys and it is grouped by the "Activity_ID" name

The last part of the code create a new table using the aggreagate function where the average of the columns mean and std is calculated for each activity and each subject in the data.

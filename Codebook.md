###Debashish Behera
##Description
Additional information about the variables, data and transformations used in the course project for the Johns Hopkins Getting and Cleaning Data course.

##Variables
###x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
###x_data, y_data and subject_data merge the previous datasets to further analysis.
###Features contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features, a numeric vector used to extract the desired data.
###A similar approach is taken with activity names through the activities variable.
###All_data merges x_data, y_data and subject_data in a big dataset.
###Finally, averages_data contains the relevant averages which will be later stored in a .txt file. ddply() from the plyr package is used to apply colMeans() and ease the development.

##Section 1. Merge the training and the test sets to create one data set.

After setting the source directory for the files, read into tables the data located in

###features.txt
###activity_labels.txt
###subject_train.txt
###x_train.txt
###y_train.txt
###subject_test.txt
###x_test.txt
###y_test.txt
Assign column names and merge to create one data set.

##Section 2. Extract only the measurements on the mean and standard deviation for each measurement.

Create a logcal vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others. Subset this data to keep only the necessary columns.

##Section 3. Use descriptive activity names to name the activities in the data set

Merge data subset with the activityType table to cinlude the descriptive activity names

##Section 4. Appropriately label the data set with descriptive activity names.

Use gsub function for pattern replacement to clean up the data labels.

##Section 5. Create a second, independent tidy data set with the average of each variable for each activity and each subject.

Per the project instructions, we need to produce only a data set with the average of each veriable for each activity and subject
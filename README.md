# Getting-Cleaning-Data
Description of the script:
The run_analysis.R script merges the training and the test sets to create one data set for further analysis.

First it checks to see if the required "reshape2" has been installed and then loads the "reshape2" package.

It then reads all required .txt files and labels them.

Subsequently the relevant "activity_id"'s and "subject_id"'s are added to the data sets and they are then combined into one single data.

All the columns with mean() and std() values are extracted using the "grep" function and then a new data frame including the "activity_id", the "subject_id" and the mean() and std() columns, is created.

With the "merge" function, descriptive activity names are merged with the mean/std values dataset, to get one dataset with descriptive activity names.

Using "melt" and "dcast" functions of the "reshape2" package, the data is converted into a table containing mean values of all the included features, arranged by the activity name and the subject id, and the data is written to the "tidy_movement_data.txt" file.

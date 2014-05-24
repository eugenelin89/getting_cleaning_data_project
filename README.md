Course Project, Johns Hopkins Data Science, Getting and Cleaning Data
=====================================================================
##### Objective of the project
* To demonstrate the ability to collect, work with, and clean a data set.
* To prepare tidy data that can be used for later analysis.

##### Deliverables
* A tidy data set with average of each variable for each activity and each subject described in the **Cleaning Raw Data** section.
* A link to this Github repository.
* A Code Book, included in this Github repository
* A Readme, included in this Github repository

##### Data Source
Data is collected from the accelerometers from the Samsung Galaxy S smartphone.  A full description is available [here.](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones)
The data for the project is available [here.](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip)



##### Cleaning Raw Data
###### 1. Merges the training and the test sets to create one data set.
* a. Horizontally merge X_train, subject_train, and y_train
* b. Horizontally merge X_test, subject_Test, and y_test
* c. Vertically merge dataframe from a and b

###### 2. Extracts only the measurements on the mean and standard deviation for each measurement.
* grep() was used to identify indices of feature names that contain **mean** or **std**.
* With data frame from step 1, only columns of the above indices are extracted.

###### 3. Uses descriptive activity names to name the activities in the data.
* Load activity labels
* Append activity label in front of our mean/std data set.
* Use merge() to merge activities with data_activity_label.

###### 4. Appropriately labels the columns with descriptive names.
* Get a vector of descriptive column labels from mean_std_index (vector of indices), features (table of features for means and stds).
* Subset the features of means and stds fream the features table.
* Extract only the descriptive name.
* Set The first column of our final table to "Activity".
* Finally, rename the columns of our table.

###### 5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.
* Using aggregate to group the data.
* Clean the result by dropping unwanted columns.
* Renaming the grouping columns.




##### Discussion of the result





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
* From features.txt, find index of mean() and std().  grep() was used to identify indices of feature names that contain **mean** or **std**.

###### 3. Uses descriptive activity names to name the activities in the data.

###### 4. Appropriately labels the columns with descriptive names.

###### 5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

##### Discussion of the result





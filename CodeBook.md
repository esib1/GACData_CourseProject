##Data Source
Download here: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

##Data Set Information
The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. 

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.

Characteristics: Multiveriate, Time-Series
Num of Instances: 10299
Num of Attributes: 561

Primary source for description: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

##Description of Data Set Files
'activity_labels.txt': Ties the class labels with their respective activity name

'features_info.txt': Details about the variables on the feature vector

'features.txt': List of features

'README.txt'

####Test

'test/X_test.txt': Test set

'test/y_test.txt': Test labels

####Training

'train/X_train.txt': Training set

'train/y_train.txt': Training labels

####Test/Train Intertial Data

'[test/train]/subject_[test/train].txt': One row per subject who performed activity for each window. Its range is from 1 to 30

'[test/train]/Inertial Signals/total_acc_[x/y/z]_[test/train].txt': Acceleration signal from the smartphone's accelerometer z/y/z axis (standard gravity units 'g'). Every row is a vector of 128 elements

'[test/train]/Inertial Signals/body_acc_[x/y/z]_[test/train].txt': Body acceleration signal obtained by subtracting the gravity from the total acceleration

'[test/train]/Inertial Signals/body_gyro_[x/y/z]_[test/train].txt': The angular velocity vector measured by the gyroscope for each window sample (in radians/second)

##Transformation details

1. Merges the training and the test sets to create one data set
2. Extracts only the measurements on the mean and standard deviation for each measurement
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive activity names
5. Creates a second, independent tidy data set with the average of each variable for each activity and each subject

##Script implementation:

Uses the reshape and data.table libraries
Loads test and train data
Loads features and activity labels
Extract the mean and std dev column headers and data
Process test data
Process training data
Merge data set and outputs as "tidy_data_esib1.txt"

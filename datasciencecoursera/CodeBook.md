Code Book
========================================================

**Data Source**

These data are derived from the Human Activity Recognition Using Smartphones Data Set, which provides accelerometer data from Samsung Galaxy S II smartphones worn by 30 volunteer subjects while they performed each of 6 activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING). The data were provided in a processed form where raw accelerometer values were converted to 561 feature variables that express different aspects of the wearer's motion. The full set of observations was divided into a training and test dataset.

**Processing**

1. The provided .zip file was extracted to the folder "UCI HAR Dataset" in the working directory and the directory structure of the .zip file was maintained.
2. The test and training data sets were both provided broken into 3 text files corresponding to the subject, activity, and feature variables respectively. These three files were merged to create unified test and training datasets. It was assumed that the ordering of observations in the 3 files was the same.
3. Test and training data sets were appended to produce a single large dataset.
4. Of the 561 features, only those corresponding to the mean and standard deviation of a measurement were kept.
5. The files "features.txt" and "activity_labels.txt" were used to assign descriptive labels to the feature variable columns and activity codes respectively.
6. Finally, the data were summarized by taking the mean of all feature variables by activity and subject.

**Data Set Description**

*Dimensions*: 180 observations on 67 variables

*Variables*:

- Subject: integer codes corresponding to the 30 different volunteer subjects
- Activity: 6 different activities performed (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING)
- Features: there are 65 feature columns named in a standardized format: dF-s-a
    + d = domain, t for time domain and f for FFT frequency domain
    + F = feature, the aspect of the motion being measured:
        - BodyAcc
        - GravityAcc
        - BodyAccJerk
        - BodyGyro
        - BodyGyroJerk
        - BodyAccMag
        - GravityAccMag
        - BodyAccJerkMag
    + s = summary statistic for feature, mean and std (standard deviation)
    + a = axis, X, Y, or Z

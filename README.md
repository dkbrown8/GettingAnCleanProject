# GettingAnCleanProject

This repository contains data output from a test conducted using a smartphone.  The data output is from the various movement sensors within a Samsung Galaxy phone.


There 2 different data sets. One is a test data set.  The other is a train data set.  The directory structure of each data set is the following:

- Root Folder
  This folder contains the activities label file, features file, feature info file and the README file.  The 
  activities files contains the labels for the different activities done by the subject during the test.  
  This file can be used to   create a factor variable in the final output of each data set.  The features 
  file contains variable names in the sensor data output file.  This file can be used named the variables 
  in the data frame created by importing the sensordata output.  The features info file describes how the variables named.
  - test folder
        This folder has the sensor output file, which has a prefix of "X", the activities file, which has a prefix 
        of "Y", and the subject_info file.  The sensor has all of the output of the sensors is somewhat raw form.  
        The activities file contains a record for each observation in the sensor output file to indictate the activity
        that was being peformed by the subject during the observation.  The subject info file contains a record for
        for each observation in the sensor output file to specify the subject that was peforming the the test.

  - train folder
        This folder has the sensor output file, which has a prefix of "X", the activities file, which has a prefix 
        of "Y", and the subject_info file.  The sensor has all of the output of the sensors is somewhat raw form.  
        The activities file contains a record for each observation in the sensor output file to indictate the activity
        that was being peformed by the subject during the observation.  The subject info file contains a record for
        for each observation in the sensor output file to specify the subject that was peforming the the test.

The purpose for this script to merge the 3 files in the test and train subfolders.  To merge the 3 files the follow these steps.

1. Import the sensors observation file into a data frame.
2. Import the features file into a data frame
3. Modify the feature name in the features data frame to remove any unwanted characters from the feature name
4. Using the feature data frame, update the column names of the senors data frame
5. Import the activities file into data frame
6. Create a new variable for the name of the activity
7. Combine the activity name variable in activity data frame with sensors data frame into a new data frame
8. Combine the subject id variable with the newly created data frame.
9. Modify the name of the subject id and activity variable in the new data frame
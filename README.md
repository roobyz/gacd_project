## Analysis of Human Activity Recognition - Using Smartphone Data

### My R script **(run_analysis.R)**, does the following:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

### run_analysis.R code summary:

#### Download the Smartphone data file.
    fileUrl <- "https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip"
    zipFile = "./UCI_project_data.zip"
    download.file(fileUrl, destfile = zipFile, method = "curl")

#### Unzip file data
    unzip(zipFile, exdir="./")
    list.files("./")

#### Start processing the data
    library(dplyr)
    library(stringr)

#### Specify the location of the phone data
    smartPhoneData = "./UCI HAR Dataset";

#### Read in the list of all features from the training set
    features = paste(smartPhoneData, "features.txt", sep="/") # name/location of file
    featuresDF <- read.table(features) # read features into a data frame```

#### Identify the columns to keep
    measurements <- filter(featuresDF, grepl('mean\\(\\)|std\\(\\)', V2))$V1

#### Remove special characters from the column header
    colfeatures <- str_replace_all(featuresDF$V2, "[^[:alnum:]]", "")

#### Load the descriptive activity labels
    activityLabel = paste(smartPhoneData, "activity_labels.txt", sep="/")
    activityLabelDF <- read.table(activityLabel)

#### Loop through the training and the test sets and merge to create one data set.
    if (exists("combineDF")) rm(combineDF)
    for (set in c("train", "test")) {
        # set the folder path for the specified data set
        tData = paste(smartPhoneData, set, sep="/")

        # get list of files from the specified data set
        tFiles = dir(tData); tFiles

        # assign the filenames to the training data
        tLabel <- paste(tData, tFiles[4], sep="/"); # descriptive labels
        tSubj  <- paste(tData, tFiles[2], sep="/"); # subject IDs
        tSet   <- paste(tData, tFiles[3], sep="/"); # subject data sets

        # read the subject data
        tSubjDF <- read.table(tSubj)
        colnames(tSubjDF) <- c("subject")

        # read the subject's signals data
        tSetDF <- read.table(tSet)
        colnames(tSetDF) <- colfeatures # add the clean column names

        # retain only the measurements columns for the mean and standard deviation
        tSetDF <- tSetDF[,measurements]

        # get the labels for the activities
        tLabelDF <- read.table(tLabel)

        # combine all the data frames for the specified set.
        tempDF <- cbind(tLabelDF, tSubjDF, tSetDF)

        # join the activities labels to the data frame
        tempDF <- merge(activityLabelDF, tempDF, by.x="V1", by.y="V1", all=T)
        tempDF$V1 <- NULL # remove the activity code field
        colnames(tempDF)[1] <- "activity"

        # row combine the training and test data sets.
        if ( !exists("combineDF") ) {
            combineDF <- tempDF
        } else {
            combineDF <- rbind(combineDF, tempDF)
        }
        # clean up the big data frame
        rm(tempDF)
    }

#### Clean up the environment.
    rm(list=setdiff(ls(), c("combineDF")))

#### Summarize the data by subject and activity
    combineDF <- group_by(combineDF, subject, activity)
    myData <- summarise_each(combineDF, funs(mean))

#### Write summary file
    write.table(myData, file="myData.txt", row.name=FALSE)



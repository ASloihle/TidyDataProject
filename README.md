# TidyDataProject
To begin, the "test" data set was loaded in, along with the "subjects" and "labels" for the test set, and the "features" document which was used for both the test and training sets.

Next, a data frame ("lbldf") was created with the activity labels ("STANDING", "WALKING", "SITTING", etc.), and the numbers 1-6 from the "labels" data that was previously loaded. The numbers were assigned the name "labelNum", the activity labels were assigned the name "labelName". This was then merged with the "testlabels" object (the "y_test" file from the original files downloaded for the assignment), and renamed "testlabels".

Finally, the labels and subjects were attached to the test data set using the "cbind" command. This gives us a complete and accurately labeled "test" data set.

The preceeding steps were then repeated exactly for the "train" data set. The "test" and "train" sets were then merged together, using the "rbind" command, to create the "finalbind" dataset, which included both sets of data and the appropriate subjects and labels. 

Because we want to only look at the mean and standard deviation of each set of measurements taken for each activity, many columns representing other calculations were removed. 
From here, two new objects were created. The first, "sublist" was simply a list of the unique values present for all the subjects in the study. A similar list, called "actlist" was created for all the unique values present in "labelName". Finally, an empty dataset with the same subject, activity, and measurement labels as "finalbind" was created. This empty data set was named "resultset".

To create the final data set, we found the mean for each measurement of each subject's activity. Upon looking more closely at the newly merged and labeled data set, it was apparent that some subjects performed only one activity, while others did more. We found the mean for each measurement of each activity that each subject actually did by using a for loop. In the loop, it first checks to see if there are values for a particular activity, and then uses sapply to find the mean for values that are present. These means are then put into the "resultset" data frame. We are left with a data frame that includes each subject, the activity or activities that they performed, and the mean of each measurement taken for each activity.


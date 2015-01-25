For the 'test" data set:

"testdata" is the actual values collected from the experiments.

"testlabels" are numerical values that map the different activities performed by the subjects to their friendly names.

"testsubjects" is a set of numbers, each representing one subject in the experiment. 

For the "train" data set:

"traindata" is the actual values collected from the experiments.

"trainlabels" are numerical values that map the different activities performed by the 
subjects to their friendly names.

"trainsubjects" is a set of numbers, each representing one subject in the experiment. 

For the combined data set:

"features" contains the names of each measurement taken for each activity, such as 

acceleration in a particular direction. These are the variables such as "tBodyAcc-mean()-Y3"

"finalbind" is the data set created by attaching activity and subject labels to the 
"train" and "test" sets, and then merging them. Columns representing measurements other 
than the ones we are interested in were removed.

"resultset" is the dataset that contains the mean for each measurement of each activity in 
"finalbind"

List of codes

featurestest <- X_test.txt
featurestrain <- X_train.txt
datafeatures is created with rbind usign featurestest and featurestrain

activitytest <- Y_test.txt
activitytrain <- Y_train.txt
dataactivity is created with rbind using activitytrain and activitytest

subjecttest <- subject_test.txt
subjecttrain <- subject_train.txt
datasubject is created using rbind using subjecttrain and subjecttest

subjact is created usign cbind(datasubject, dataactivity)
fulldata is created using cbind(datafeatures, subjact) - fulldata is the ONE resulted dataset by merging feature, activity and subject

mstdfulldata is created and contains the measurements with mean and std, activity, subject

Uses the file activity_labels.txt to replace the corresponding activity in the mstdfulldata, taken from the file activity_labels.txt 

t means Time
f means Frequency
Acc means Accelerometer
BodyBody means Body 
Gyro means Gyroscope
Mag means Magnitude
mean() means Mean
std() means STD
mstdfulldata is the tidy dataset resulting of this process

finaldata summarized data taking the means of each variable for each activity and each subject, grouped by subject and activity

Export finaldata into Final_data.txt file
# Run_analysis
This is the code for getting tidy data gleaned by Samsung wearable equipment in an experiment

The raw data can be accessed via https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

In the tidy data sumbitted, we have 6 columes:
(1) activity: int. 1,2,3,4,5,6  ## the number of activity in which data was recorded in the experiment
(2) subject: int. 1,2,...,30  ## the number of subjects in the experiement
(3) variable: char. ## variable of data recorded in the experiment
(4) value: num. ## the mean of the measurement for the variable grouping by subject and activity
(5) activity_name: char. ## name of the activity 1=walking; 2=walking upstairs; 3=walking downstairs; 4=sitting; 5=standing; 6=laying

Here is the pseudo code for getting the final tidy data:
1. read the train and test raw data, and merge them into one big data file
2. change the column names to descriptive names
3. extract the data whose column names include "mean" or "std"
4. match the activity with descriptive names
5. read the final data into txt file

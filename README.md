# Datacamp-project--Data-Analyst-Associate-Practical-Exam Submission
Datacamp workspace link:
https://app.datacamp.com/workspace/w/eff75a70-a5ba-4da7-aee2-6aebecf5f9ab#data-analyst-associate-practical-exam-submission

Certificate:
https://www.datacamp.com/certificate/DAA0016893970215


## Data Validation

Describe the validation tasks you performed and what you found. Have you made any changes to the data to enable further analysis? Remember to describe what you did for every column in the data.

Write your description here

The original data is 98 rows and 8 columns. The first thing I did was to get the info. I found that the "Claim Amount" column's dtype which is a object does not match with the dataset criteria. I first coverted the claim amount columns from string to integer by removing "R$" & "," then changing the data type to numeric. Second, I found that 78 rows 'Cause' value was missing, I replaced the NaN rows with ‘unknown’ value. There were no missing values values of the data set.

There are 98 unique Claim ID, as expected
The "Time to Close" column is numeric as expected but cannot confirm why there was a value with -57 day so keep the data unchange
"Amount Paid" was numeric as expected
There were 4 Location of claim, as expected
"Individuals on Claim" is numeric as expected
There are 2 Linked Cases options - True/False, as expected.

## Data Discovery and Visualization

Describe what you found in the analysis and how the visualizations answer the customer questions in the project brief. In your description you should:

Include at least two different data visualizations to demonstrate the characteristics of single variables
Include at least one data visualization to demonstrate the relationship between two or more variables
Describe how your analysis has answered the business questions in the project brief
Write your description here

## How does the number of claims differ across locations?
There are four claim loccation included in this data. The highest claim location is SAO LUIS, with RECIFE being second. Third is FORTALEZA and the fourth is NATAL.

Breakdown by category
![Count_different_claims_location](https://user-images.githubusercontent.com/112617394/204235775-72647493-cdd2-4ba2-8aaf-7d1551ae1453.png)

## What is the distribution of time to close claims?
The new head of the legal department wants to see if there are differences in the time it takes to close claims across the locations. We should look at how the time to close claims is distributed. According to Time to close claims, we can see that most places have had less than 1500 Days. There are some outliers that get more than 3000 to 3500 Day to close claim but this is very uncommon.

![Distribution_of_time_to_close_claims](https://user-images.githubusercontent.com/112617394/204236411-4b8fae5c-e908-407b-9359-91ed429656cd.png)

## How does the average time to close claims differ by location?

Finally we want to combine the two pieces of information to see how the location impacts the day of time to close claims. We need to look at the two variables together to see if this is realistic.

We could see the visualization of the data on previous graph. To show the impact, we can look at the range of time to close claim by location and we marked the white circle point to indicate the average of time to close claims for each location. SAO LUIS include the highest time to close claims and the interquartile range is also the higher than other 3 location. SAO LUIS and RECIFE average time are slightly below the median line but FORTALEZA and NATAL average time are above the median and fall into the upper quartile. Although FORTALEZA and NATAL have relative short range of interquartile but the they included some outliner claims which take longer time to close claims brings the average up.

Based on all of the above, we would recommend that the team further investigate SAO LUIS Claims case as it has diversity clase claims time and 1 case below is zero. Further analysis should be done to understand aby other factor to improve the performance if location really does impact the time to close claims. The team should also consider including other factor for analysis. So that we can further analyze other potential variable such as Claim Amount, Individuals on Claim , and Cause may impacts over time.

![Time_to_close_claims_by_location](https://user-images.githubusercontent.com/112617394/204236569-d3e8ba59-a1b1-4f42-babb-43c1937412d6.png)

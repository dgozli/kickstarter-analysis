# Kickstarting with Excel

## Overview of Project

### Purpose

This project intended to understand some of the factors associated with the outcome of kickstarter campaigns (success, failure, or cancel) belonging to the general category of theater and plays. We wanted to inform Louise, who was interested in running a campaign of her own with the goal of raising $12,000 dollars. Our project had two aims. First, we asked whether there was a link between the outcome of campaigns and the month in which the campaigns were launched. Second, we asked if there was an association between campaign outcomes and the monetary goals of the campaigns.

## Analysis and Challenges

Analyses were conducted in Excel on the raw Kickstarter data (4113 rows x 10 columns). Two main analyses were conducted, the first examining the link between outcomes and launch dates (month of year), and the second examining the link between outcomes and goals (amount of money). 

### Analysis of Outcomes Based on Launch Date

The result of the first analysis is summarized in Figure 1 (Theater_Outcomes_vs_Launch.png), which is based on the pivot table on the Excel sheet "Theatre Outcomes by Launch Date." With the pivot table, we selected only "theater" campaigns in this analysis, counting successful, failed, and canceled outcomes. We decided to use "months" as the time variable, collapsing across years. 

### Analysis of Outcomes Based on Goals

The results of the second analysis is summarized in Figure 2 (Outcomes_vs_Goal.png), which is based on the summarized data on the Excel sheet "Outcomes based on Goals." In this case, data were filtered with Excel's countifs() function, to include only "plays" campaigns divided into 12 groups based on their goals. 

### Challenges and Difficulties Encountered

In the first analysis, one challenge I faced was in creating the "Years" variable, which served as a filter in the pivot table. For some reason, Excel failed to apply the Years() function to all the rows and I had to repeat the extension of the formula several times. Finally, the Years column was completed after multiple tries. 

In the second analysis, the possible challenge had to do with the application of up to four simultaneous conditions in the countifs() function, which was difficult to track. The manual application of the countifs() function to each cell (i.e., copying-and-pasting with modification) was inefficient for me. If we had 100 conditions, instead of 12, the process would have been very time consuming.

## Results

We can draw two conclusions from the first analysis (Outcomes by Launch Date). (1) The proportion of successful campaigns has been highest in May and June, but that is partly because the total number of campaigns launched is higher in those months. By contrast, the proportion of successful campaigns is at its lowest in December. This suggests that Louise might have a better chance launching her campaign in May. (2) The number of canceled project does not seem to vary much based on launch date, although we see the largest number of canceled projects starting in January and least (zero) canceled projects in October. 

Additionally, we can draw two conclusions from the second analysis (Outcome Based on Goals). (1) The ratio of successful to failed projects is highest with the smallest goals (less than $5K), whereas the ratio is at its lowest with the largest goals ($45K or more). (2) Aside from the extreme goal values, there is no straightforward relationship between Goals and Outcomes, which means it is difficult to predict campaign outcomes for goals of between $5K to $45K.

An important limitation of our data set was that it did not include enough data points that could be compared with Louise's planned campaign. Louise was interested in launching a $12K campaign for her play, but about 85% of the campaigns in the "play" subcategory had a goal of less than $10K. That made it difficult to make inferences from our data that could be directly applicable to Louise. In general, there are not enough data points corresponding to goals larger than $15K, which means it is difficult to get an accurate sense of the relationship between Outcomes and Goals. 


## Possible Additional Analysis 

We could conduct additional analysis to inspect the connection between Outcome and "Staff_pick" variable. A related variable is "Spotlight," which could similarly be related to the outcome. We could include a bar graph that includes both Staff_pick (x-axis) and Spotlight (different colors of bars) as variables and our dependent variable would be percentage of successful campaigns (y-axis). 

We did not examine the duration of campaigns (the length of time between launch date and the deadline), and whether that was related to outcomes. Therefore, we could also include a line graph, whose x-axis would be the length of campaign and the y-axis would be the count of outcomes.
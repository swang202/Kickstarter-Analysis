# Kickstarting with Excel

## Overview of Project

In order to help Louise to determine the best fundraising strategies for her play *Fever*, we collected data of 4114 campaign projects from 2009 to 2017. Projects included nine main categories: film and video, food, game, journalism, music, photography, publishing, technology, and theater. 

### Purpose
To find out the best month to launch the project and the optimal fundraising goal, we investigated the effect of the launching date and the funding goals in relation to the campaigns outcomes using the dataset collected.

## Analysis and Challenges
Data was converted into interpretable format before the analysis. Analysis of the campaign outcomes based on their launch dates and their funding goals were conducted using pivot table. Both results were visualized using line graphs.

### Analysis of Outcomes Based on Launch Date
In order to analyst the outcomes based on goals, we created pivot tables using following steps: 
1. Set the "parent category" and "years" as filters.
2. Filtered on the "Parent Category" to show only the data for "theater".
3. Grouped the launched date (after converted to interpretable dates) of each projects into each of the twelve months.
4. By putting the outcomes into column value and filtering, the numbers of "Successful", "Failed", and "Canceled" of each projects and the total projects in each month were counted.

### Analysis of Outcomes Based on Goals
In order to analyst the outcomes based on goals, we created pivot tables using following steps: 
1. Set up ranges of goals based on the dollar-amount with an increment of $5000.
2. Filtered on the "Subcategory" column using "plays" as the criteria.
3. The numbers of "Successful", "Failed", and "Canceled" projects were counted in each goal ranges.
4. In each goal range, the sum of total projects and the percentage of the successful, failed of canceled campaign were calculated.

### Challenges and Difficulties Encountered
- The dataset contains time data (Unix epoch time) that are not interpretable, thus initial conversions were required. 
- Main category and subcategory were combined into one column. For certain analysis, researchers need to separate the category and subcategory in separate columns.

## Results
- Outcomes based on Launch Date
  - By comparing the outcomes of each month, we noticed that in the summer between May, June and July. 
  - Generally, the number of successful cases is higher throughout the year, except for December.

![Outcomes based on Launch Dates](https://github.com/swang202/Kickstarter-Analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png?raw=true)

- Outcomes based on Goals
  - When diving the outcomes by number of goals, we discovered that most of the goals were set less than $5000 (67.1% of all projects).
  - In projects which the goal was set to less than $1000 or in between $1000 to $4999 has a higher successful rate (76% and 73%, respectively) compare to failed projects within the same range (24% and 27%, respectively).
  - There are no canceled campaign in plays.

![Outcomes based on Goals](https://github.com/swang202/Kickstarter-Analysis/blob/main/Resources/Outcomes_vs_Goals.png?raw=true)

- Limitations of the dataset
  - The id of each projects started with 0, which might cause some confusion.
  - The label of certain categories are not well defined, such as "staff_pick", thus makes the data uninterpretable.

- Future directions
  - In evaluation of the outcomes by launch date, more analysis and graph could be helpful.
    - The total number and percent of projects launched by month in a line graph.
    - The percent of project outcomes launched in each month in a bar graph with stacking by outcomes.
  - In evaluation of the outcomes based on goals, there are couple improvements needed.
    - The goals were separated with an increment of 5000 until 50000, which contains categories that only have very few projects.  
    - Percentages are not the best way to represent the data. For the goal ranges with only one or two projects, the percentages are not representative due to low project number.

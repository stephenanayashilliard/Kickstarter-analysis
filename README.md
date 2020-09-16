# Kickstarting with Excel
## Overview of Project
### Purpose
- The following analysis compares how well different fundraising campaigns for theatrically produced plays fared
in relation to the dates the plays were officially produced and their individual funding goals.
## Analysis and Challenges
- My analysis was based on two questions;  does the launch time frame for a production effect its success rate?, and does the amount of the fundraising goal have any effect
on its success?  To compare the launch dates vs succcess rates, I first needed to convert from unix time stamp to a standard time format.  This was done using the formula: =(((J2/60)/60)/24)+DATE(1970,1,1).  From there, the year was extracted and a pivat table was created based on the percentage of successful, failed and canceled productions.  

![Pivot table: Outcomes Based on Launch](https://github.com/stephenanayashilliard/Kickstarter-analysis/blob/master/Pivot%20table%2C%20Outcomes%20Based%20on%20Launch%20Date.png)

There were no challenges with the data itself besides reformating the pivot table success rates into percentages and making sure that all percentage outcomes were rounded to zero decimal points.  
- To answer the question does the amount of the fundraising goal have any effect on its success, I needed to create a spread sheet breaking down the goal amounts in $5000.00 increments ranging from less than $1000 to greater than $50000.   I also need to create columns refleting the number of successful, failed and canceled projects.  Since data was pulled from an excel sheet that also included productions in other genres, I needed to filter out all other data except plays.   To accomplish this, I used the following formula, with changes made for each row and column. =COUNTIFS(Kickstarter!D:D, "<1000", Kickstarter!F:F, "successful", Kickstarter!R:R, "plays")  When all formulas were applied, this is how the final spreadsheet appeared:  

![Spread sheet: Outcome based on Goals](https://github.com/stephenanayashilliard/Kickstarter-analysis/blob/master/Spread%20sheet%20%2COutcome%20Based%20on%20Goals.png)

From the "Outcome based on Goals" spread sheet, a pivot table was created.

![Pivot Table:  Outcomes Based on Goals]

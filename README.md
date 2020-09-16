# Kickstarting with Excel
## Overview of Project
### Purpose
  The following analysis compares how well different fundraising campaigns for theatrically produced plays fared
in relation to the dates the plays were officially produced and their individual funding goals.
## Analysis and Challenges
  My analysis was based on two questions;  does the launch time frame for a production effect its success rate?, and does the amount of the fundraising goal have any effect
on its success?  To compare the launch dates vs succcess rates, I first needed to convert from a unix time stamp to a standard time format.  This was done using the formula: =(((J2/60)/60)/24)+DATE(1970,1,1).  From there, the year was extracted and a pivot table was created based on the percentage of successful, failed and canceled productions.  

![Pivot table: Outcomes Based on Launch](https://github.com/stephenanayashilliard/Kickstarter-analysis/blob/master/Pivot%20table%2C%20Outcomes%20Based%20on%20Launch%20Date.png)

  There were no challenges with the data itself besides reformating the pivot table success rates into percentages and making sure that all percentage outcomes were rounded to zero decimal points.  The reformatting was very important to take care of in the pivot table otherwise the the pivot chart was difficult to read and esthetically unpleasing.

  To answer the question does the amount of the fundraising goal have any effect on its success, I needed to create a spread sheet breaking down the goal amounts in $5000 increments ranging from less than $1000 to greater than $50k.   I also needed to create columns reflecting the number of successful, failed and canceled projects.  Since data was pulled from an excel sheet that also included productions in other genres, I needed to filter out all other genres except plays.   To accomplish this, I used the following formula, with changes made for each row and column. =COUNTIFS(Kickstarter!D:D, "<1000", Kickstarter!F:F, "successful", Kickstarter!R:R, "plays")  When all formulas were applied, this is how the final spreadsheet appeared:  

![Spread sheet: Outcome based on Goals](https://github.com/stephenanayashilliard/Kickstarter-analysis/blob/master/Spread%20sheet%20%2COutcome%20Based%20on%20Goals.png)

From the "Outcome based on Goals" spread sheet, a pivot table was created.

![Pivot Table:  Outcomes Based on Goals](https://github.com/stephenanayashilliard/Kickstarter-analysis/blob/master/Pivot%20table%2C%20Outcomes%20Based%20on%20Goals.png)

Once again, there were no challenges using Excel formulus themselves, however, there were challenges creating the charts and graphs.  There were visuals in the presentation that were time consuming. Having to move the graph's Key around or changing Font types so they would fit, are some examples of esthetic challenges.  As I increase my skill in Excel, these issues will become less time consuming.

### Analysis of Outcomes Based on Launch Date

![Outcomes Based on Launch Date](https://github.com/stephenanayashilliard/Kickstarter-analysis/blob/master/Resources/Theater_Outcomes_vs_Launch.png)

Examining the graph above there are two conclusions one can make:
  1. The best time to launch a new play production is during the Spring quarter with a May launch giving the best possible chance of a successful launch.
  2. Production success starts a steady decline in the summer months, however,  a launch in December is most likely to lead to a failed launch.

### Analysis of Outcomes Based on Goals

![Outcomes Based on Goals](https://github.com/stephenanayashilliard/Kickstarter-analysis/blob/master/Resources/Outcome_vs_Goals.png)

The graph "Outcomes Based on Goals"  is based on the percentage of successful, failed and canceled productions and the goal amounts set during their fund raising efforts.  All canceled productions were at zero percent in all fund raising categories.   The successful and failed productions rates, however, are mirror images of each other.  From the graphic it appears that fundraising goals set at under $5000 are more likely to be successful with a study decline in that sucess rate as the funding goals increase.  There is a marked uptick in success rates at the 30k to 50k mark which could be explained by the fact that there are so few plays funded at this level, so therefore a successful launch of a small number of productions can make the appearance that there is a greater chance of success than there is in actuality.

### Data set limitations
Although the data's findings do provide  clear indicators of when is the best time period to launch a production, as well as what funding goals are most likely to lead to success, data detailing the play's genre might provide a clearing understanding;  for example, how many plays can be classified as  drama's or comedies, or how many plays were new productions or revivals?

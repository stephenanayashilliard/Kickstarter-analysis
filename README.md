# Kickstarting with Excel
## Overview of Project
### Purpose
- The following analysis compares how well different fundraising campaigns for theatrically produced plays fared
in relation to the dates the plays were officially produced and their individual funding goals.
## Analysis and Challenges
- My analysis was based on two questions;  does the launch time frame for a production effect its success rate?, and does the amount of the fundraising goal have any effect
on its success?  To compare the launch dates vs succcess rates, I first needed to convert from unix time stamp to a standard time format.  This was done using the formula: =(((J2/60)/60)/24)+DATE(1970,1,1).  From there, the year was extracted and a pivat table was created based on the percentage of successful, failed and canceled productions.  

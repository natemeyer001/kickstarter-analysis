# Kickstarting with Excel

## Overview of Project

### Purpose
Explore trends in previous Kickstarter campaigns to increase likelihood of success for a Kickstarter campaign. Starting broadly with all the data, then narrowing in on campaigns more similar to our friend, Louise.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
After some initial analyzation of the entire data set, it was apparent that not all campaigns are created equally and I needed to restrict my data. The first restriction was on the category to get only "theater" since that's what Louise's is. After that filter the data was ready to be turned into a pivot table shown below.

![Theater-Outcome-Pivot](https://user-images.githubusercontent.com/30487641/125222914-7e799f80-e290-11eb-835b-1ee2cb60e074.png)

The rows are by months (for all years) and the columns are sorted to have "successful" first since that is what we are most interested in. The only challenge was playing around with the rows to display the data by month, which required deleting some fields that auto-genereated when the Year field was selected.
Using the pivot table, I created the following chart to better visualize the data.

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/30487641/125223004-a6690300-e290-11eb-8c30-d0604ce18264.png)


### Analysis of Outcomes Based on Goals
That was a good start, but it included all of "theater" instead of just "plays", and it also treated a project with a goal of $500 the same as a project with a goal of $50,000. So, I created a new table with goal amounts banded mostly in 5k increments, which split up the data nicely. I also made sure to only include plays this time to get a more accurate picture to compare to Louise's. I converted the raw numbers into percentages to show a clearer picture.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/30487641/125223373-49ba1800-e291-11eb-8f64-42059894281a.png)


### Challenges and Difficulties Encountered
For the Launch Date pivot table there were some extra fields that populated when the field "Year" was selected, but it was easy enough to delete them. For the Goals analysis, the main challenge was minimizing typing. I accomplished that by using absolute references to the Kickstarter worksheet in my COUNTIFS statements. In addition, I copied and pasted the formula for the "Goal of $1,000 to $4,999" to the below cells and edited the ranges to reduce typing. I then copied that column to the right for failed and pasted "failed" over the "successful" for all cells. I did the same thing for canceled.


## Results
**What are two conclusions you can draw about the Outcomes based on Launch Date?**
The chart displays a clear spike in successful campaigns starting in May and going through July, as well as a sharp decline for Nov and Dec. Interestingly, the number of failed stays relatively stable throughout the year. Thus, it would appear that launching late spring/early summer has the highest likelihood of succeeding even though there is lots of competition. Additionally, launching towards the end of the year spells trouble as the amount failed almost catches up to the amount successful.

**What can you conclude about the Outcomes based on Goals?**
In general that higher the goal, the lower the chance of success. However, between 35k and 45k the data bucks the trend - although there are only nine such projects in that band compared to the overall number of over one-thousand. Also, over 90% of the data has goals less than 15k, and in that sample the negative relationship between goal and success rate is more apparent as pictured below.

![Outcomes_Based_On_Goals_15k](https://user-images.githubusercontent.com/30487641/125223604-a9b0be80-e291-11eb-955c-b95caadc10b9.png)


**What are some limitations of this dataset?**
There is no accounting for who set up/shared the campaign - was it one person in Ely, MN with no social media following? Or was it a set up/shared by a team of savy social media experts who shared it to their large following? Also, the data tells us the total donations as well as the number of backers, which allows us to calculate average donation, but does not provide info on the distribution of donations or the timing of the donations. One hypothesis is that campaigns are more likely to be successful if a big donation is done early on, but that is not testable given the data.

**What are some other possible tables and/or graphs that we could create?**
Outcomes based on average donation. Outcomes based on length of time to reach goal.

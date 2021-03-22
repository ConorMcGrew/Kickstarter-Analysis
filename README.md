# An Analysis of Kickstarter Campaigns

## Overview

Louis is an up-and-coming playwright. She is attempting to use crowdfunding to create her play, *Fever*, and estimates a budget of $10,000. We were tasked with determining what factors may benefit (or harm) her chances of funding *Fever* by looking at various other Kickstarter campaigns.  

## Analysis

When first looking at the data, the first thing to notice is that a great many of the kickstarter campaigns had nothing to do with plays, or even theater for that matter. The first challenge, then was to break the data down into only that pertinent for Louise. 
<img width="981" alt="Screen Shot 2021-03-21 at 7 41 48 PM" src="https://user-images.githubusercontent.com/80495710/111928629-97183c80-8a8a-11eb-94c7-cf0157341acd.png">

The category and subcategory data was initially combined, and we had to separate it out to filter it. 

Another big hurdle was the outcome column. 

<img width="497" alt="Screen Shot 2021-03-21 at 7 38 54 PM" src="https://user-images.githubusercontent.com/80495710/111928667-ab5c3980-8a8a-11eb-9dd1-75802cc55645.png">

There was no obvious conclusion about the outcomes of the campaigns, only the goal and pledged amounts. 

Once a sufficient number of useful filters had been added, various pivot tables were generated in order to represent the data most relevant to Louise. 

![Theater Outcomes](https://user-images.githubusercontent.com/80495710/111928792-ff671e00-8a8a-11eb-8bc4-e2aed630eaf0.png) 

So to begin the analysis we looked at outcomes from the specific parent category of theater and noticed a success rate of 58%. However, more specifically, for the subcategory of plays the success rate of funding was a surprising 65%. Since Luoise had a very specific goal in mind ($10,000), the sheer success rate didn't seem adequately descriptive. We then turned to descriptive statistics of the parent category of theater. 

<img width="285" alt="Screen Shot 2021-03-21 at 7 43 53 PM" src="https://user-images.githubusercontent.com/80495710/111928714-c9c23500-8a8a-11eb-8a93-35e0670cb106.png">


The mean goal and mean pledged amounts, $5,049 and $5,602 respectively, made it seem as though the campaigns were, on average, unsuccessful. However, the standard deviation for the goals was $7,749 and the standard deviation for pledged amounts was $8,335. This implies that there are several goal and pledged amounts that skew the distribution right (a few very large pledged and goal numbers that disproportionately affect the mean and spread of the data). Thus, we resorted to looking at quartiles instead, noting that even the 3rd quartile (i.e. the lower 75% of the data) pointed toward success as the most likely outcome for a theater kickstarter (as the 3rd quartile of the goal amount was $5,000 and the 3rd quartile of the pledged amount was $5,699). This, unfortunately, created a new challenge. Louise’s goal was $10,000, but the reason so many campaigns seemed to be successful were their relatively low goal amounts. 

We then turned to a more comprehensive way of displaying the data relevant to Louise. We first generated a pivot chart for outcomes of theater kickstarters organized by when they were launched, in order to give Louise a good window of when she should launch her campaign. Then we generated a table for play outcomes based on their goal amounts. This will give Louise the best information on success rates for her particular goal of $10,000. 

The greatest challenge was making sure that all of the filters were appropriately applied to pivot tables and conditional formating was appropriately auto-applied. With such a large data set, it would take a very long time to enter each formula and filter individually, so letting Excel take some of that load off meant being very careful in how my formulas were generated. When I discovered missteps it was often that I didn’t have absolute references or that I was attempting to filter for something I hadn’t generated yet. 

## Results

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/80495710/111928869-3fc69c00-8a8b-11eb-9f44-50270eeb75ba.png)

The *Theater Outcomes by Lauch Date* indicate that May is the peak point at which to launch a campaign, as it has the highest success rate at 67%. Additionally, June has a very high success rate at 65%, July has a success rate of 63%, and even February has a success rate of 63%. This suggests that midyear is an ideal time to launch her campaign. However, into months with high expenses (such as August when children usual start back to school or January/Decemeber for holidays) the kickstarter is almost as likely to fail as it is to succeed. So it is recommened that she not launch then.

![Outcomes vs Goals](https://user-images.githubusercontent.com/80495710/111928893-566cf300-8a8b-11eb-90c8-6773889b6f1f.png)

Since Louise already had a budget of $10,000, the outcomes based on goals gives her the best idea of how successful her campaign will be. As stated earlier in the discussion of the data distribution, the campaigns with relatively small goals (less than $1,000 and between $1,000 and $4,999) have over 70% success rates. However, the bracket that Louise’s goal fits into has a 54% success rate, and even if she could narrow costs to be in the next bracket ($5,000 to $9,999) she would only increase her chances to 55% success rate. In general, as the goal amount increases, the percentage that get funded decreases. It is my recommendation that she try to sort her costs by what can be done totally in advance (such as set assembly, costumes, etc.) versus what needs to be done closer to time for production (finding talent, establishing a venue, etc.). Hopefully, even though $10,000 is her pre-production budget, we can split it into two separate campaigns, each of which will be in the $1,000 - $4,999 bracket. The things that can be done entirely in advance could be funded in May, while the second campaign is launched in June/July, thus boosting the odds of her overall goal being funded. 

The biggest limitation, is that while the kickstarter data is vast, we don’t have an extensive amount for plays just like Louise’s. Only 72 other plays fit in the same cost bracket as hers, and those aren’t necessarily from the same city as Louise (I would imagine that people are more likely to fund a production if it is local) or if those campaigns had some buzzwords that really invested people in them. Additionally, because there are so few campaigns with goals greater than $15,000, it is hard to say whether raising her cost of production to $35,000 would actually increase her chances of achieving that goal (as seen in the chart it has a 67% success rate but that is represented by just 4 of 6, not 200 of 300 *per se*). Additionally, the *Theater Outcomes Based on Launch Date* looks somewhat misleading. It has only the number of successes and failures. I think it would give a more accurate relationship if it were based on percentage (as the two primary categories always have at least 30 members). 

We should probably generate a similar charts filtered by theater production parent category and outcome, but filtered by just the goals that are within a reasonable amount to cut / add from Louise’s budget ($8,500 to $11,500 for instance). Then generate a chart to see if the success rate was at all affected by certain buzzwords present in the blurbs, or if the subcategory it was listed under had any affect (plays versus musical for instance). Moreover, I think some further analysis should be done on the outcomes by launch date for May, June, and July to show exactly why those months were so successful, and perhaps get all the way down to what specific day she should launch it on (day of the month versus outcome). 


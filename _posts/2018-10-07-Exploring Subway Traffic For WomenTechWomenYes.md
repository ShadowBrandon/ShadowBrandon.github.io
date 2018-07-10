---
layout: post
title: Introduction
---

# Exploring Subway Traffic For WomenTechWomenYes 

## The Challenge
WomenTechWomenYes (WTWY), a non-profit organization in New York City, is raising money for their annual gala. 
To promote the event, street teams are being placed outside subway stations to hand out free gala tickets.
WTWY want to use  MTA subway data to optimize the placement of their street teams to gather the most signatures, 
ideally from those who will attend the gala and contribute to their cause.

## The Methods

Our approach was taking MTA Turnstile Data from April 1, 2018 - June 30, 2018 since we believe that the gala would
benefit from campaining two to three months before the gala starts. From there, our group cleaned up the data set by 
removing duplicate data, removing negative counts, cap 4 hour intervals at 50,000, and remove days with 0 riders.
It is worth noting that only 5 percent of the data had one of these characteristics. 

![Image test]({{https://github.com/ShadowBrandon/ShadowBrandon.github.io/tree/master}}/Images/MTAWeighting.png "Abstract Method of Cleaning")

In the first wave of data analysis, we looked at results of ridership by various variables.

Our group developed a second wave of data analysis when we analyze the "% IT Residents by Zipcode" and linking the 
zipcode to a trainstation in NYC since providing recomendations based on areas with strong presence of IT residents
would provide a stronger likelihood to gather the most signatures, attend the gala, and contribute to WTWY's cause.

Finally, our group did a "Ridership Was Weighted by Percent IT Residents" . doing The following provides a rough formula
of the score card, where those with the highest number were our best recomendations for sending outreach:

![Image test]({{https://github.com/ShadowBrandon/ShadowBrandon.github.io/tree/master}}/Images/MTACleaning.png "Method of Weighting")

## The First Wave of Results -

#### Top 10 MTA Stations 

![Image test]({{https://github.com/ShadowBrandon/ShadowBrandon.github.io/tree/master}}/Images/MTARidership.png "Top 10 MTA Station Ridership no weight")

#### Number of Week in Spring for Canvassing

![Image test]({{https://github.com/ShadowBrandon/ShadowBrandon.github.io/tree/master}}/Images/WeeklyRidership.png "Weekly Ridership")

#### Days of the Week to Canvass

![Image test]({{https://github.com/ShadowBrandon/ShadowBrandon.github.io/tree/master}}/Images/DailyRidership.png "Large example image")

## The Second Wave of Results -

![Image test]({{https://github.com/ShadowBrandon/ShadowBrandon.github.io/tree/master}}/Images/WeightedTop10.png "Top 10 MTA Station Ridership (weighted)")


## The Recommendations from General Analysis and Weighted Scores Analysis
### Canvass at MTA stations with:
* High ridership in April-June
* High proportions of information workers living in the same zip code as the station
### Canvass at MTA stations when: 
* Tues-Thurs
* All Spring weeks equally good
### Station from high priority to low-priority:
![Image test]({{https://github.com/ShadowBrandon/ShadowBrandon.github.io/tree/master}}/Images/FinalizedListedTop10.png "Top 10 MTA Station Ridership List (weighted)")

END~~~
-------------------






























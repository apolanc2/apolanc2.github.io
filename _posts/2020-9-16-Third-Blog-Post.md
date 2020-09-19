---
layout: post
title: Project 1 
---
# Project 1: NHL API
## Data Setup
For project 1, we were assigned the task of creating a vignette for reading and summarizing data form the National Hockey League's API. 
To do this there were 2 main functions created.    
  1. **nhlRecords**: This function has one required argument, "endpoint" here you can call in the specific endpoint. There is also one optional argument, "franchiseID". 
  If desired, you can enter in the franchise ID to filter for a specific franchise.    
  2. **nhlStats**: This function as no required arguments. If this is used without arguments, it will return all stats! For modifications set "modifier" equal to your desired modification. To modifiy the stats there is the "teamID" and "season" arguments.
  to capture a specific team, please set "teamID" equal desired ID number. If specific seasons are desired set "season" equal to desired season year. If multiple seasons are desired please identify all season years side by side without spaces. For example if you are interested in 2015 and 2016 then season="20152016".    
To make it easier for the user, a wrapper function, **nhlAPI(interest)** was created so there was only one function needed to get to these endpoints. 
Here "interest" is either a nhlRecords endpoint or it is a nhlStats modifier. By default this function is read to call in an endpoint, when stats are desired "stats" must be set equal to "TRUE". The rest of the arguments noted from the functions above can be used accordingly.

I have also created 2 vectors that have the endpoints and stats modifiers for quick applications! No need to double check your spelling!
  "endpoints" stores the 5 different endpoints and "modifier" stores the 8 different modifiers.

## Exploring the Data
### Franchise and Season Data
The first pieces of data I decided to explore were the franchise and season records endpoints. I joined these two by franchiseId, but first I had to rename ID from the franchise endpoint to "franchiseId".
I ended up creating 2 new variables, startyr and endyr. To create startyr I took the first 4 characters from the firstSeasonId, to get what I imagine is the year of their first season. To create endyr I tok the first 4 characters from the lastSeasonId, to get what I imagine is the year of their last season.
Then I created frequency tables for both wins and losses against the start year. To avoid a scary large frequency table, I grouped the wins and losses by 20.
I decided to also create summary tables for win streaks and loss streaks. At a quick glance it looks like the home streak tends to be higher than the road win streak and the loss home streak tends to be lower than the road loss streak.
To see a breakdown of win streak by team I used a bargraph. I felt the best way to view this was in descending order!

### Team Total stats by franchise
I combined the team total stats with the franchise information.
I created new variables to show the start year and end year. Using the start year I was able to calculate the number of years were active as of the current year. To explore this data based on years active I grouped the active years by 20. In addition to this, I calculated the win rate and the home win rate.
Now we are able to explore the win rates based on the amount of years the team has been active!
First we explore this with box plots for both rates. We quickly notice that there are 0 teams that have been active for 60-79 years, but we don't notice an immediate trend. It does look like teams active for more than 80 years may have an overall better win rate for home games, but we can't be too sure.
Next we can explore the win rate using a histogram. In general, we can see that the rates tend to be in between 0.4 and 0.5.
Lastly, we can explore both the win rate and the home win rate together using a scatter plot. We can see that as the win rate increases the home win rate generally increases as well, which may indicate teams do better at their home.

## Reflection
Looking back on how I approached the project, I don't know that I would have done anything really different. I do think commiting to github from RStudio was a bit intimidating.
Now that I have accomplished this I feel more confident about using github in the future, which would allow me to be a bit more efficient.
Overall, the most challenging part of the project was getting RStudio and github to communicate. I ran in to a lot of issues and received many fatal errors. Unfortunately, since github pages requires the repository to be public, I ran into a lot of these issues last minute. To be sure my page was functioning I had to sacrifice the table of contents. 
I also found understanding the data to be a bit difficult. Generally, before diving into data I like to have more of a background. As a clinical analyst, I don't always have a lot of information on the data I work with and I've become accustom to it. I will say NHL data was very new to me, but I enjoy exploring and learning new things. 
Programming wise, I felt the most difficult part was retreiving the data. There are a lot of resources out there to figure out different functions if you forget, but since every API isn't the same it can be difficult!
Moving forward the best piece of advice I could give myself or anyone else is "Don't panic, you know what to do!"
 
[My Repo Link For Project1](https://apolanc2.github.io/Project1/)

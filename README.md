# Test_Nespresso
## Summary:
First we read and load some basic libraries and functions that we need  
I had some trouble with the warnings so i make a command to ignore them  
As the timestamp variable presented some issues of formating that would be a trouble in the future, we first read the timestamp in te data normally and the cange it to integer  
## 1.What is our daily overall clickthrough rate? how does it vary between groups?  
The Clickthrough rate usually is used to "somehow" measure the user engagement (i say somehow because it helps understand engagement, although it is useless if you only see this kpi for trying to explain it, there are many factor to take into account like if they finally went to the end of the pipeline and bought the product or the why they click, if it was a mistake, if they were just curious, etc), by definition is the proportion of search sessions when the user clicks on one of the possible options.  
In order to understand the average clickthrough rate of the users, we use a groupby clause, moreover if we want to do on a day basis we use a gruopby day to finally count the number of search performed in that period of time. Then its just work of dividing these numbers to obtain the rate we want "Daily_avg = CT_x_Day / Searches_x_Day".  
Here we can appreciate that it varies from 0.24 to 0.36 for the overall rate. now lets take a look to compare between the groups of the case:  
In this case we just need to do the same reasoning and code as before but now making the program to perform it making distinction between the groups a and b:  
You can see and conclude that group a customers tend to have a much bigger number that B group members, more or less 0.35 for a members and 0.25 for b members 

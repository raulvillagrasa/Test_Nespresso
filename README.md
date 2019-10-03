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
You can see and conclude that group "a customers" tend to have a much higher CTR number that B group members, more or less 0.35 for a members and 0.25 for b members.  

## 2.Which results do people tend to try first? How does it change day by day?
We can tell which page has been visited by getting building "result_position variable" of the page that was visisted, we do this using the groupby by day, session_id and result position. (we are interest in values that exist, that means that the result must be grater than 0), then we print the headers to see how is going:  
Then we run the code over the number of days and count the result_positions of the pages that were first visited and order them by result_position. we sort the dataframe is in chronological order so we can tell that the result we get back is based by the first search (I hold only the first 10 result positions becasuse after that we see that the number is practically meaningless).  
Looking at the results we can make some preliminar observations like:  
  

## 3.What is their daily overall zero results rate? How does it vary between the groups?  
KeFirst we keep only the day of our date, and because we are only interested this time in the zeros we just study where  'n_results'=0 and divide by the number of searches, this should give us the the zero rate for each day  
Then we create "zero_res_groups" which is made the same way as above, but also group by the 'group', that is telling me if the session is in 'group a' or in 'group b' and we use the previous results to see that:  
The average zero rate is almost the double in group b than group a. 


# Summarize of relevant findings:
1. The first result is the most popular, somehow it makes sense because (asusuming that usually the IT and crm team assign the marks in the web in order they will appear to customers and in order of relevance also, so you offer the most interesting and engaging webs first, then the second one ando so on...)
2. Also you can see that the clicks have some kind of stationality, where it shows that most days the first search results get about 2300-2500 clicks, but it drops in click rate for the first search result occurs on the 5th day. We can also see the same pattern happens for the clickrate for the second result
3.when analizing the zeros you see that it makes sense with the prevous information, since group b has a smaller clickthrough rate and having zero search results would result in less clickthroughs.






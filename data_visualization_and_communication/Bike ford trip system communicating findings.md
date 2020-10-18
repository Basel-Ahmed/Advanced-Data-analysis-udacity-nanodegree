
# Dataset oveview
## Data source:
- Ford GoBike System Data : https://www.fordgobike.com/system-data This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area .
- I chose to analyse trips in 2019:8 
## Features :
The Features included in the Data are as follows :

* Member Year of Birth
* Member Gender
* User Type (Subscriber or Customer – “Subscriber” = Member or “Customer” = Casual)
* Trip Duration(in seconds)
* Bike ID
* Start Time and Date
- End Time and Date
- Start Station ID
- End Station ID
- Start Station Name
- End Station Name
- End Station Latitude
- End Station Longitude
- Start Station Latitude
- Start Station Longitude


# Questions we can answer 
1. What are types of users for ford bike system and distribution of each type
2. How long durations of trips in the system
3. what are differences in duraion of trips between user types
4. What are the stations that alot of trips start from
5. what are the stations that alot of trips end at 
6.  what are the most repeated trips 
7. what are types of bikes exist and distribution of each type
8. what type of bikes each user type use
9. which type of bikes is used for longer trips
10. what are times in the day that has most occuring trips 
11. what are the times each user type make a lot of trips

# main finidings
1. We have 2 types of users (subscribe , customer) the subscribe type dominate user types with percentage of 81% 
    - by drawing bar plot for 'user_type' variable 
2. Most trips has smaller durations and few has long duration
    - by drawing histogram plot for 'duration_sec' variable and zoom in the skewed part of data 
3. generally customer user type make longer trips than subscribe user type
    - by drawing box and violin plot for 'duration_sec' variable for each user type
4. We have 4 stations that alot of trips start from 
    - by drawing bar plot for start_station_name and choos the first 4 highest counts
    - San Francisco Caltrain Station 2  (Townsend St at 4th St)    5101
    - Berry St at 4th St                                           4005
    - Market St at 10th St                                         3460
    - San Francisco Ferry Building (Harry Bridges Plaza)           3196
5. We have 4 ststions that a lot of trips end at 
    - San Francisco Caltrain Station 2  (Townsend St at 4th St)  
    - Montgomery St BART Station (Market St at 2nd St)             
    - San Francisco Ferry Building (Harry Bridges Plaza)           
    - Berry St at 4th St 
6. We have 2 equally repeated trips in the data 
    - from san francisco ferry building to embracadero at sansome5t 
    - Berry 5t at 4th 5t to san francisco ferry building(Hsrry bridges plaza)
        - by creating a new variable that combine start_station_name and end_station_name separated by comma and draw bar plot for it  
7. We have 2 types of bikes exist one can be shared for all trips and one type can not be shared which is the dominant type with percentage of 93%
    - by drawing bar plot for 'bike_shared_for_all_trips'variable 
8. we can say that bikes that are shared for all trips are not available to customer user as they have ability to pay premium prices  
    - and in general there  is a preference for non shared bikes
    - by drawing clustered bar plot 
9. The bikes that are not shared for all trips are used for  slightly longer trip duration than those are shared
    - by drawing box and violin plot for each bike type
10. Most trips happen from 6:00 AM to 6:00 PM
    - by creating a new column (day_quarter) derived from start_time column and then divide 24 hours into 4 parts(Q1,Q2,Q3,q4) 
11. Subscribe user type have more trips from 6:00 am to 12:00 pm than any other time in the day but customer user type have more trips from 12:00 pm to 6:pm
    - by drawing clustered bar plot for day_quarter variable and user_type variable
    
    
    



# What we can do futher 
- What we can do further is knowing which weeks has more trips by creating a new variable that represent week number 1:7 is the first week , 8:14 second week and so on and then draw bar plot to count number of trips in each week
- which week has trips that has longer durarion by drawing box plot for each week 
- we can also know at which week subcribe user type make more trips 


# Key insights to convey 
1. We have 2 types of users (subscribe , customer) the subscribe type dominate user types with percentage of 81% 
2. Most trips has smaller durations and few has long duration
3. generally customer user type make longer trips than subscribe user type 
4. We have 4 stations that alot of trips start from 
    - San Francisco Caltrain Station 2  (Townsend St at 4th St)    5101
    - Berry St at 4th St                                           4005
    - Market St at 10th St                                         3460
    - San Francisco Ferry Building (Harry Bridges Plaza)           3196
5. We have 4 ststions that a lot of trips end at 
    - San Francisco Caltrain Station 2  (Townsend St at 4th St)  
    - Montgomery St BART Station (Market St at 2nd St)             
    - San Francisco Ferry Building (Harry Bridges Plaza)           
    - Berry St at 4th St 
6. We have 2 equally repeated trips in the data 
    - from san francisco ferry building to embracadero at sansome5t 
    - Berry 5t at 4th 5t to san francisco ferry building(Hsrry bridges plaza)
7. We have 2 types of bikes exist one can be shared for all trips and one type can not be shared which is the dominant type
8. we can say that bikes that are shared for all trips are not available to customer user as they have ability to pay premium prices  
    - and in general there  is a preference for non shared bikes

9. The bikes that are not shared for all trips are used for  slightly longer trip duration than those are shared
10. Most trips happen from 6:00 AM to 6:00 PM
11. Subscribe user type have more trips from 6:00 am to 12:00 pm than any other time in the day but customer user type have more trips from 12:00 pm to 6:pm

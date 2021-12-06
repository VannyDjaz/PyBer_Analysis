# PyBer_Analysis

# Visualizing Ride-Sharing Data for a ride sharing app I.vualize.
## Ride sharing from January 01 2019 through May 2019.
_In this project will be using Python graphing library Matplotlib to get accurate data for _
In this project, I first had to combine date into single data set. Using this code; 
## pyber_data_df = pd.merge(ride_data_df, city_data_df, how="left", on=["city", "city"]) I had managed to get results and as you can see on Pyber challenge, South Michelleport had more ride shares around 2019-03-04 at 18:24:0 in the amount of $30.24	with rider_ID 2343912425577 and	72 rides in the	Urban area.

I wanted to also pull out sum of fares by type, for that I used to this code; 
## sum_fares_by_type = pyber_data_df.groupby(["date", "type"]).sum()["fare"].reset_index() to group the date, type and fares. 

I also wanted to merge both DataFrame and getting the average fare per rider for each city;
# new_df = pd.merge(urban_avg_fare, urban_driver_count, how= "inner", on=["city", "city"])

### PIVOT TABLE

To get evven more accurate data by columns, values, and index I have created a pivot table using pivot(). Code used: 
## pyber_data_df.pivot = pyber_data_df.pivot(index="date", columns="type", values="fare"), with this code I got data that were not readable so I had to create another table to pull up a whole week sum ride, fares and type using also the resample() method, I was able to get a clear vision, with January 20 2019 being the month with the highest fare both in the suburban as well as the Urban area and January 13 2019 with the lowest fare in the rural area. 

### Line Graph representing ride shares;

I was also requested to get graph fivethirtyeight matplotlib using df.plot() function, after running the following codes, I was able to get a graph representing thay in fact rural area is a better area for ride shares with the highest fares all from January 2019-Begining of May 2019. It will be good to put more drivers in the urban area because of the demand that way it will compasate for the rural area with low demand in ride shares, by doing so they won't be a huge gap in the revenue. Even Though in May it goes down, it looks like in the suburbs and rural area it will still compasate for that month of May.
# I was able to create the graph syle and using this code: 
 1.style.use('fivethirtyeight')
 2.new_df = new_df.plot(figsize = (20,6))

#End of my presentation. Thank you

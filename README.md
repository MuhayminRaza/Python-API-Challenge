# Python-API-Challenge

This challenge has 2 parts: WeatherPy and VacationPy. WeatherPy involved trying to visualize the weather of over 500 cities of varying distances from the equator. VacationPy is useful in planning future vacations. The starter code was obtained from the course notes. 

The following code was written with the help of a TA through office hours: 
From WeatherPy:

city_data_df.plot.scatter(x = "Lat", y = "Wind Speed")
plt.title("City Latitude vs Wind Speed")
plt.xlabel('Latitude',fontsize =10)
plt.ylabel('Wind Speed (m/s)')
plt.show() 


plt.scatter(northern_hemi_df["Lat"],northern_hemi_df["Max Temp"],color='g')
plt.plot(northern_hemi_df["Lat"], regress_values, color='red')
plt.annotate(line_eq,(45,36), fontsize=10)
plt.xlabel("Latitude")
plt.ylabel("Max Temp") 
plt.title("Temperature vs. Latitude Linear Regression Plot (Northern)")
plt.show()



From VacationPy:

city_humidity_map = city_data_df.hvplot.points("Lng", 
                                      "Lat", 
                                      geo = True,  
                                      tiles = "OSM",
                                      frame_width = 800,
                                      frame_height = 500,
                                      size = "Humidity",
                                      scale = 1,
                                      color = "City")
                                      
new_hotel_map = hotel_df.hvplot.points("Lng", 
                                   "Lat", 
                                   geo = True,
                                   color = "City",
                                   alpha = 0.8,
                                   size = "Humidity",
                                   tiles = "OSM",
                                   hover_cols = ["Hotel Name", "Country"])

# Transport
Nice addition to Israeli apps
Recently the minister of transportation decided to make new payment rates that depend on distance.
This application calculates the distance and tells the user how much he needs to pay



Highlights:

        location1 = self.google_maps.search(location= self.address1.get("1.0", "end-1c"),) # sends search to Google Maps.
        location2 = self.google_maps.search(location= self.address2.get("1.0", "end-1c"),) # sends search to Google Maps.
        my_location1 = location1.first() # returns only first location.
        my_location2 = location2.first() # returns only first location.
        coords_1 = (my_location1.lat, my_location1.lng)
        coords_2 = (my_location2.lat, my_location2.lng)
        dis = geopy.distance.geodesic(coords_1, coords_2).km
        
        if dis <=15.0:
            self.label1 =Label(text= "You are in the YELLOW zone 5.5 shekel is your payment ",font=("Helvetica", 12),background= 'yellow')
        elif dis >15.0 and dis <=40.0:
            self.label1 =Label(text= "You are in the GREEN zone 12 shekel is your payment ",font=("Helvetica", 12),background= 'green')
        elif dis >40.0 and dis <=75.0:
            self.label1 =Label(text= "You are in the LIGHT BLUE zone 16 shekel is your payment ",font=("Helvetica", 12),background= 'light blue')
        elif dis >75.0 and dis <=120.0:
            self.label1 =Label(text= "You are in the BLUE zone 16 shekel is your payment ",font=("Helvetica", 12),background= 'blue')
        elif dis >120.0 and dis <=225.0:
            self.label1 =Label(text= "You are in the PURPLE zone 27 shekel is your payment ",font=("Helvetica", 12),background= 'purple')
        elif  dis >225.0:
            self.label1 =Label(text= "You are in the GRAY zone 68.5 shekel is your payment ",font=("Helvetica", 12),background= 'gray')
        self.label1.place(x=170,y=100)

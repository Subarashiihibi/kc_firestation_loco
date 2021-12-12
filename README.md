# Final Project: Seattle Fire Station Locator
Application URL:
Repo URL: 

# Description:
As Seattle‘s weather condition, fire has long been an issue from long time ago in Seattle.
As a result, the Seattle Fire Station Locator is built to help the user to query the information 
of nearby fire stations in the neighborhood of the place they are interested in.By building this
simple Web GIS application, I hope this would be of help for those homeowners to know what options 
they have when a fire suddenly comes and they could do whatever they could to save  themselves before 
the firefighter come to rescue, for the newly coming residents who are seeking a safe housing location
that are close enough or have multiple close contact with fire stations nearby.

# Web Application Functions
As introduced, the web application is a fire station locator. The sidebar contains the information
of the fire stations and the address of each of them. The Web application allow user to query their interested 
place from the search bar on the upper right corner of the map. The intended function of the map is when the query is made, 
a pop-up on closest fire station's marker will occur, showing the details of the fire station including
its address and number of the fire station, which is stored in the geojson file. The bounding box for the 
query would mainly limit the query area in most of area in Seattle, so the user can only access the information of places 
in Seattle. Other areas are not included for users to query. The search function of the Seattle Fire Station Locator is achieved 
with Geocoder controls. 

# Screenshot
![Screenshot of Fire Station Locator](https://user-images.githubusercontent.com/80044018/145708299-88de7cdf-ea57-4a40-a8b8-57ddf62b4514.png)


# Main Functions
## Location query using Geocoder
The search bar on the upper corner is implemented using the geocoder controls for the users to conduct queries in location.
The bounding box includes most of the areas in Seattle. Just like any search engine, users could type in their preferred location,
the camera will zoom in to your intended location. The user could confirm the queried place to let it show in the map of Seattle area. 

The side bar contains the fire station information, including the fire station number (for distinguishing brances and HQs), the post code
of the fire station as well their addresses. If the user click on the side bar, the matching fire station will have a pop-up on it showing these pieces of
information. As the user could close the pop-ups, the web page allow the user to check the information of fire stations without refreshing the original page
because the zoom-in level of both querying place and clicking on fire stations has been adjusted so most information could be generated. 

# Functions may come in the future
## Calculation of Distance and Routes using Turf.js
I also attempted to add some functions such as calculating the distance between queried place and the nearest fire station，but I failed to do so because JavaScript
cannot modify the external geojson file and I cannot add new feature properties "distance" in the geojson file to help achieve the goal. Still I will try my best to add such functions in the future which could greatly enhance the user experience.


# Data Source
King County GIS data Portal  
<https://gis-kingcounty.opendata.arcgis.com/datasets/fire-station-locations-in-king-county-firestn-point/explore?location=47.501600%2C-121.937850%2C10.26>  
(The data is open to public, generated on March 9th, 2005 and last updated on Dec 3rd, 2018)


# Applied Libraries
geocoder API, Mapbox GL JS, 
For sharing the application, Github is used to publish the content and store the data applied in the program. 
The maki markers of the map comes from Mapbox as well.

Hopefully could use Turf.js to add the distance and routes calculation of queried place and the closest fire station in the future if I have chances. 

# Acknowledgements
I am very appreciative to Prof. Zhao and Teaching Assitant Steven's help on the course and finishing the project. Only with their patience could the project have been done. 

# Other Notices
Generally, the emergency contact is still recognized as 911. The contact information of Seattle Fire Stations for non-emergency issues, however,
is (206)-386-1400. Some users may find it is possible to find the fire stations outside Seattle border in the web application; however, as mentioned before,
the query bounding box is mainly limited the search in most Seattle borders, so you may not find the fire stations that are nearby in the place searched typed
in the search bar since there will not be search results for such region. The fire station data, as also mentioned, was lastly updated on Dec, 3rd, 2018. This 
might cause problems because urban area has been constantly changing so some of the constructions might no longer be there or new fire stations might have already occured
with no records in the data from King County GIS data portal. Before making decisions upon the small application please think twice and refer to official information on 
location of fire stations because this is not an official web application created by Seattle Government.

The framework of the web application is largely inspired by the Store Locator in the tutorial of Mapbox GL JS. The web application may still have a lot of places to improve.
If you find something important in the texts and the web application, you could freely leave your advice or comments at my GitHub repos. I might add more functionalities 
into this small application in the future, such as adding routes and finding the closest fire station to your queried result. 


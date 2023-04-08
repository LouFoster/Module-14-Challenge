# Module-14-Challenge

##Overview

(As captured from Data Bootcamp Module 14) 

In this module, as assigned Data Analyst, I will populate a geographical map with GeoJSON earthquake data from a URL. Each earthquake will be visually represented by a circle and color, whereas a higher magnitude will have a larger diameter and will be darker in color. In addition, each earthquake will have a popup marker that, when clicked, will show the magnitude of the earthquake and the location of the earthquake.

By the end of this module, as assigned Data Analyst, I will complete the following::
    •	Create a branch from the main branch on GitHub.

    •	Add, commit, and push data to a GitHub branch.

    •	Merge a branch with the main branch on GitHub.

    •	Retrieve data from a GeoJSON file.

    •	Make API requests to a server to host geographical maps.

    •	Populate geographical maps with GeoJSON data using JavaScript and the Data-Driven Documents (D3) library.

    •	Add multiple map layers to geographical maps using Leaflet control plugins to add user interface controls.

    •	Use JavaScript ES6 functions to add GeoJSON data, features, and interactivity to maps.

  •	Render maps on a local server.


##Purpose

(This module is built around a project that mirrors a real-world scenario that would require data analysis and visualization.)

In module 14, I will practice analysis, visualization, and statistical skills by retrieving and analyzing severe weather, in particular, Earthquake related data.) Working with the Client (Basil) we have created a Basic Project Plan, to ensure this our project is successfully implemented.

##Basic Project Plan
  Purpose

  The purpose of this project is to visually show the differences between the magnitudes of earthquakes all over the world for the last seven days.

  Tasks

  To complete this project, use a URL for GeoJSON earthquake data from the USGS website and retrieve geographical coordinates and the magnitudes of earthquakes for the last seven days. Then add the data to a map.

  Approach

    My approach will be to use the JavaScript and the D3.js library to retrieve the coordinates and magnitudes of the earthquakes from the GeoJSON data. You'll use the Leaflet library to plot the data on a Mapbox map through an API request and create interactivity for the earthquake data.


##Deliverable 1: Add Tectonic Plate Data

1.	Create a new folder on your Mapping_Earthquakes repository and name it "Earthquake_Challenge."

2.	Copy the folders and files from your Earthquakes_past7days branch and add them to the Earthquake_Challenge folder. The folder should have this structure:
 
 ![image](https://user-images.githubusercontent.com/117233641/230746249-2d3e8e40-76f6-4b9e-b028-f088005fc0a1.png)

3.	Download the tectonic_plate_starter_logic.js file, add it to your js folder, and rename it challenge_logic.js.

4.	In Step 1, add a second layer group variable for the tectonic plate data.

5.	In Step 2, add a reference to the tectonic plate data to the overlay object.
 
![image](https://user-images.githubusercontent.com/117233641/230746257-1c03a9df-47ed-4072-8a70-bf303f42f506.png)

![image](https://user-images.githubusercontent.com/117233641/230746266-ae530bad-6ec9-46dc-b24b-f64631457fce.png)

6.	In Step 3, using d3.json() callback method, make a call to the tectonic plate data using the GeoJSON/PB2002_boundaries.json data from this GitHub repositoryLinks to an external site. for the tectonic plate data. You’ll need to log into GitHub to access the GeoJSON data.

![image](https://user-images.githubusercontent.com/117233641/230746273-6978f499-b858-4a6b-899e-f437e3f7303d.png)

7.	Inside the d3.json() method do the following:

  o	Pass the tectonic plate data to the geoJSON() layer.

  o	Style the lines with a color and weight that will make it stand out on all maps.

  o	Add the tectonic layer group variable you created in Step 1 to the map, i.e., .addTo(tectonicPlates) and close the geoJSON() layer.

  o	Next, add the tectonic layer group variable to the map, i.e, tectonicPlates.addTo(map).

  o	Finally, close the d3.json() callback.

 ![image](https://user-images.githubusercontent.com/117233641/230746286-8e853612-8dd8-47c2-8e7c-0498555187dd.png)

8.	Start your Python server and launch the index.html file and confirm that your map with the earthquake and tectonic plate data is similar to the following image.

 ![image](https://user-images.githubusercontent.com/117233641/230746290-9ecc70d2-5437-47c0-a12b-8c4bf991a66e.png)

![image](https://user-images.githubusercontent.com/117233641/230746296-d10ee1b8-c9d9-460c-af30-6a91c7842286.png)


##Deliverable 2: Add Major Earthquake Data
1.	In Step 1, add a third layer group variable for the major earthquake data.

 ![image](https://user-images.githubusercontent.com/117233641/230746299-abfb1184-ae99-4c4f-8636-ee8cc749a01b.png)

2.	In Step 2, add a reference to the major earthquake data to the overlay object.

![image](https://user-images.githubusercontent.com/117233641/230746304-78f91c56-fc4a-4577-b758-34768c0196eb.png)


3.	In Step 3, use the d3.json() callback method to make a call to the major earthquake data from the GeoJSON Summary Feed for M4.5+ EarthquakesLinks to an external site. for the Past 7 Days.

 ![image](https://user-images.githubusercontent.com/117233641/230746306-d4a020fd-4ece-41eb-8315-cc3b313d5fc5.png)

4.	In Step 4, use the same parameters in the styleInfo() function that will make a call to the getColor() and getRadius() functions.

![image](https://user-images.githubusercontent.com/117233641/230746312-0f3dd598-0bb0-4da8-b0c4-ae0e5219cf6e.png)

5.	In Step 5, change the getColor() function to use only three colors for the following magnitudes; magnitude less than 5, a magnitude greater than 5, and a magnitude greater than 6.
  
![image](https://user-images.githubusercontent.com/117233641/230746319-aebfc3a9-5e5c-4496-b96b-ba8281f2c685.png)


6.	In Step 6, use the same parameters from the preceding step in the getRadius() function.

![image](https://user-images.githubusercontent.com/117233641/230746322-343fc199-971a-4c96-b3f7-779d014e803c.png)

7.	In Step 7, pass the major earthquake data into the GeoJSON layer and do the following with the geoJSON() layer:
    o	Turn each feature into a circleMarker on the map
    
    o	Style each circle with styleInfo() function
    
    o	Create a popup for the circle to display the magnitude and location of the earthquake
    
    o	Add the major earthquake layer group variable you created in Step 1 to the map, i.e., .addTo(majorEQ) and then close the geoJSON() layer.

![image](https://user-images.githubusercontent.com/117233641/230746336-7cfaafbe-bf09-40d1-9662-971455025a11.png)

 
8.	Then, add the major earthquake layer group variable to the map, i.e, majorEQ.addTo(map), and then close the d3.json() callback.

9.	Start your Python server and launch the index.html file and confirm that your map with the two earthquake data sets and tectonic plate data is similar to the following image.

 ![image](https://user-images.githubusercontent.com/117233641/230746337-63e61e2e-4b67-47ac-874b-13fb8ba92317.png)

![image](https://user-images.githubusercontent.com/117233641/230746339-30a8c74f-8875-496a-ba22-8df05cea5051.png)

 



##Deliverable 3: Add an Additional Map

Using your knowledge of JavaScript and Leaflet.js add a third map style to your earthquake map.

1.	Using the options from the Mapbox stylesLinks to an external site., add a third map style as a tile layer object to the challenge_logic.js file.

![image](https://user-images.githubusercontent.com/117233641/230746342-e8db18ca-452d-48a8-87a9-959d73cd13de.png)

2.	Add the map variable to the base layer object.
 ![image](https://user-images.githubusercontent.com/117233641/230746353-7e2a5ad5-dee3-4503-a244-c0425f1409ac.png)


3.	Start your Python server and launch the index.html file and confirm that your map is similar to the following image, where there are three map styles, and displays the two earthquake data sets and the tectonic plate data.

 ![image](https://user-images.githubusercontent.com/117233641/230746370-45444767-6512-4c86-b44a-8dae9d84a346.png)




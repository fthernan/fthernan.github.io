---
title: ECLAC webmaps
category: Experience
order: 7
year: 2020
thumbsize: 1
tags: [maps, GIS, geographic data, programming]
---
# #ECLAC webmaps

I was hired as a consultant for the development of a web geographic data viewer. The project was commissioned by the ECLAC (United Nations Economic Commission for Latin America and the Caribbean) and consisted of a map viewer for its REDATAM webserver software, for 4 types of data: segregation, mobility, migrations and general indicators.

The segregation module allows you to select a minority (or a "minority" made up of various social groups) and calculates the interaction, Duncan and isolation indices. It also shows relevant information regarding minorities on the map, such as the percentages of representation, the weight of minorities, the percentage difference, etc.

The module of migrations allows to visualize the migratory flows, selecting an area (or several) as a reference pivot, and calculating the incoming or outgoing flow with respect to it. The bilateral migratory balance can also be calculated, and the areas that lose or gain inhabitants can be visualized on the map.

The mobility module is similar to the migration module, and allows you to carry out the same type of processing but for more general data, keeping the same options.

The general indicators module allows you to visualize numerical data on the map and show all the information related to the shape when you click on it (similar to a GIS program, including name, id, etc). The indicators can also be grouped into groups, adding the numbers and displaying the result on the map.

In addition, all the modules have map filters that allow the calculation to be limited to a specific area and a ranking filter, which allows you to see the areas with greater or lesser value of the information displayed. Maximum and minimum values, calculated areas, and total sum of the displayed variable are also shown.

The visualization allows options such as:
* Visualize by points or shapes
* Change the classification classes and classification type:
    * Equal intervals
    * Quantiles
    * Natural Jenks
    * Standard deviation
    * Arithmetic progression
    * Geometric progression
* Change the scale
* Change basemap
* Change the color palette
* The legend adjusts with respect to the selected option

Some other options such as printing, real-time language change, additional helper layers, were also added.

**The authorization to add images and screenshots of the project is being processed. As soon as they authorize me, I will upload the images here.**

<!---
![Screen 02](images/ECLAC%20webmaps/screen02.png)
*In order to improve the speed of the scraping, I used a multithreading downloading and processing*
-->

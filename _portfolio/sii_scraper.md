---
title: Sii_scraper
category: Projects
order: 4
year: 2016
thumbsize: 1
tags: [engineering, scraping]
---
# #SII scraper

*If the information exists, just scrape it!*

In 2017, the Internal Revenue Service of Chile (SII) published a webmap with information about the terrains -fiscal appraisal, type of use, etc.- and everyone was exited because it was something totally new (at least in Chile).

With some friends we had an idea about building a model, but the information didn't exists until that date, so we decided to scrape that info. But the problem was that the maps were rasterized in a WMS, and there was no way to get the shapefiles, but that was not a problem.

In order to get the information I build a software with vision superpowers. First of all, the software start to download all the tiles of the desired area in a good resolution (1024x1024 per tile) and by each tile, using openCV, I was able to get the shape that was rasterized in the image (using edge detection, polygon approximation, and some other algorithms). After getting those shapes, the next step was use a clipping algorithm to perform an union, and this was the most expensive task in the program.

After the obtaining the shapes, I started to obtain the info associated with that shape using the same program and sending some post request to the server with centroids of shapes in Web Mercator coordinates.


![Screen 02](images/sii_scraper/screen02.png)
*In order to improve the speed of the scraping, I used a multithreading downloading and processing*

The result was amazing, and all the shapes where successfully recognized as we can see on the image.


![Screen 03](images/sii_scraper/screen03.png)
*Information obtained*

Sadly, after all that work, we analyzed the data and we noticed that the information was uncompleted, so it didn't work for our purposes :(

Anyways, I was able to see some interesting info

![Screen 04](images/sii_scraper/screen04.png)
*Terrain value using area and fiscal appraisal*

![Screen 06](images/sii_scraper/screen06.png)
*Cartogram of terrain value*

links
- [SII Maps](https://www4.sii.cl/mapasui/internet/#/contenido/index.html)

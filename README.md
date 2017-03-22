# Reporting on the Dakota Access Pipeline protests of 2016.
## An analysis and visualization of federal data on crude oil spills  

The following workshop walks you through a data analysis and visualization I carried out for [Undark magazine](https://undark.org/article/oil-pipeline-safety-dakota-access-standing-rock/) on the risk of an oil spill surrounding the Dakota Access Pipeline debate. It is an introduction to finding, cleaning and visualizing federal data using Excel and Carto.com. 

### Questions I had that guided my reporting

![alt text](http://aleszu.com/workshops/oilwater1.png)

### What are some of things these protestors are so angry about?

![alt text](http://aleszu.com/workshops/oilwater2.png)

### Could DAPL rupture? If so, what is the risk?

![alt text](http://aleszu.com/workshops/oilwater4.png)

### How often do spills occur?

### When they rupture, how much oil spills?

### And where in the U.S. do these spills occur?

# How I put it together

### I found [data](https://www.phmsa.dot.gov/pipeline/library/data-stats/flagged-data-files) from the Pipeline and Hazardous Materials Safety Administration (PHMSA).

![alt text](http://aleszu.com/workshops/oilwater5.png)

### I downloaded a zip file.

![alt text](http://aleszu.com/workshops/oilwater6.png)

### The government was nice enough to tell me what every column corresponded to.

![alt text](http://aleszu.com/workshops/oilwater7.png)

### All I really had to do in Excel was filter, sort and count. 

![alt text](http://aleszu.com/workshops/oilwater8.png)

## Do the analysis yourself

For this workshop, download a filtered version I cleaned up that only has crude oil spills over 100 barrels (net lost) since 2010 [here](https://drive.google.com/file/d/0B56vzj8m6JInRWZGM0tyQk94VTA/view?usp=sharing). If you want the full zip file of PHMSA flagged incidents go [here](https://www.phmsa.dot.gov/pipeline/library/data-stats/flagged-data-files).

Try asking yourself another question and answer it with this dataset. Try asking questions on: 
1. a commodity besides crude oil 
2. the riskiest pipeline operators 
3. spills in specific states

## Build the map yourself

1. Boot up [Carto.com](http://Carto.com), create a login and upload the CSV from above. 

2. Plot the data by latitude and longitude and then style the points by net barrels recovered. 

3. To add interactivity to your map, play with the "widgets" function. Add a "histogram" pulled from one of your columns, like "net_loss_barrels," and a "category" from the "iyear" column.

4. What other geographic information might be helpful? Let's add in the shapefiles for the U.S.'s crude oil pipelines. Those can be found in a [zip](https://www.eia.gov/maps/map_data/CrudeOil_Pipelines_US_EIA.zip) from the [U.S. Energy Information Administration](https://www.eia.gov/maps/layer_info-m.php). 

5. Extra points if you can track down and plot the shapefile for the Standing Rock reservation.

Read the full story on Undark [here](https://undark.org/article/oil-pipeline-safety-dakota-access-standing-rock/).

![alt text](http://aleszu.com/workshops/carto-oilwater.png)

Link to Undark interactive map [here](https://undark.carto.com/viz/e053d3f2-b66b-11e6-a2ce-0e233c30368f/public_map) and workshop interactive map [here](https://storybench.carto.com/builder/eaeb6a08-0e47-11e7-a547-0ef24382571b/).



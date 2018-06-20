# Reporting on the Dakota Access Pipeline protests of 2016
## An analysis and visualization of federal data on crude oil spills in the U.S.

The following workshop walks you through a data analysis and visualization I carried out for [Undark magazine](https://undark.org/article/oil-pipeline-safety-dakota-access-standing-rock/) on the risk of an oil spill surrounding the Dakota Access Pipeline debate. It is an introduction to finding, cleaning and visualizing federal data using tools like Google Sheets, Excel, Datawrapper and Carto.com. 

### Questions I had that guided my reporting

![alt text](http://aleszu.com/workshops/oilwater1.png)

### What are some of things these protestors are so angry about?

![alt text](http://aleszu.com/workshops/oilwater4b.jpg)

### How often do spills occur? And when pipelines rupture, how much oil spills?

![alt text](http://aleszu.com/workshops/oilwater4.png)

### Where in the U.S. do these spills occur?

![alt text](http://aleszu.com/workshops/oilwater2.png)

### Could we map that?

![alt text](http://aleszu.com/workshops/oilwater4d.jpg)

# How I put it together

### I found [data](https://www.phmsa.dot.gov/pipeline/library/data-stats/flagged-data-files) from the Pipeline and Hazardous Materials Safety Administration (PHMSA). 

![alt text](http://aleszu.com/workshops/oilwater5.png)

### I downloaded a zip file. 

![alt text](http://aleszu.com/workshops/oilwater6.png)

### The government was nice enough to tell me what every column corresponded to.

![alt text](http://aleszu.com/workshops/oilwater7.png)

### All I really had to do in Excel was filter, sort and count. 

![alt text](http://aleszu.com/workshops/oilwater8.png)

### I dropped my cleaned up spreadsheet into Carto.com

![alt text](http://aleszu.com/workshops/carto-oilwater.png)

### And then I reported my story 

I tracked down and got sources like Rosenfeld, Stafford, Bommer, Coleman and Horn – who did the spill risk analysis for DAPL – on the line and write up an article.  

### We published it and watch it blow up on [Twitter](https://twitter.com/badhombrenps/status/824643921397555201)!

![alt text](http://aleszu.com/workshops/twitter-oilwater.png)

# Data analysis and visualization: do it yourself

For this workshop, let's start with a filtered version of the [top 20 crude oil spills](http://aleszu.com/workshops/top20crude.csv) since 2010 by size. If you want the full zip file of PHMSA flagged incidents go [here](https://www.phmsa.dot.gov/pipeline/library/data-stats/flagged-data-files).

## Data filtering and sorting

### How did I get the top 20 crude oil spills by size?

Let's first inspect the full dataset in Google Sheets. [Open this spreadsheet](https://docs.google.com/spreadsheets/d/1ZIjpP5WfUwXLCHvsjdxdxS4ngj2UrUMRb4kE3DXw_20/edit?usp=sharing) and click "Make a copy..." in the File menu. (Notice the title, hl2010toPresent, is the same spreadsheet I downloaded from the PHMSA website zip file.) Add a filter by clicking "Turn on filter" in the Data menu or clicking the filter icon.

![alt text](http://aleszu.com/workshops/sheets-oilwater.png)

### Filter by COMMODITY_RELEASED_TYPE 

We want to analyze only crude oil spills – since that's what our story is about – so we'll click the drop-down triangle next to COMMODITY_RELEASED_TYPE and click "Clear" under "Filter by values..." Next, scroll down and select "CRUDE OIL" and then click the blue "OK" button. 

![alt text](http://aleszu.com/workshops/sheets-oilwater1.png)

### Sort NET_LOSS_BBLS by highest to lowest

We want to see which crude oil spills were the largest in this dataset, so click NET_LOSS_BBLS and click "Sort Z -> A" (Notice that COMMODITY_RELEASED_TYPE has a green filter and only CRUDE OIL rows are appearing.

![alt text](http://aleszu.com/workshops/sheets-oilwater2.png)

## Exploratory data visualization

### Descriptive statistics 

Descriptive statistics is used to describe the features of a dataset. In the case of column NET_LOSS_BBLS, we'd like to know the average, the minimum, the maximum, and the count to get our heads around the data. Select the NET_LOSS_BBLS column by clicking "AE" and look at the bottom-right corner for a box listing Sum, Average, Min, Max, Count and Count Numbers. What do you notice about these spills? 

![alt text](http://aleszu.com/workshops/sheets-oilwater2.png)

Let's do the same for the UNINTENTIONAL_RELEASE_BBLS column and compare the Sum, Average, Min, Max, and Count.

## Mapping with Datawrapper.de

1. Go to [datawrapper.de](http://datawrapper.de) and click "Create a Map." Then, click "Symbol maps."

![alt text](http://aleszu.com/workshops/datawrapper-oilwater.png)

2. Search for "USA" and click "USA » US-States"

![alt text](http://aleszu.com/workshops/datawrapper-oilwater2.png)

3. Under add your data, click "import your dataset" button, click import dataset by latitude and longitude, and upload a [CSV like this one of the top 20 crude spills by size](http://aleszu.com/workshops/top20crude.csv).

![alt text](http://aleszu.com/workshops/datawrapper-oilwater3.png)

4. Next, adjust the column that will be mapped to the "size" of the symbols. Select "NET_LOSS_BBLS." Click "Proceed" at bottom of page.

![alt text](http://aleszu.com/workshops/datawrapper-oilwater4.png)

5. Click "Set symbol tooltip" to map some data to points that will be revealed once a user hovers over them. I've decided to put ONSHORE_COUNTY NAME and ONSHORE_STATE_ABBREVIATION in the title and NET_LOSS_BBLS in the body of the tooltip. You can add text, commas, colons and some basic HTML like a line break <br /> to design the tooltip. Scroll down and click "Save."

![alt text](http://aleszu.com/workshops/datawrapper-oilwater7.png)

6. Click the "Annotate" tab and add a title like "Top 20 crude oil spills since 2010." 

![alt text](http://aleszu.com/workshops/datawrapper-oilwater5.png)

7. Click "Publish" and on the next page click "Publish Chart." Copy the URL or embed code. 

![alt text](http://aleszu.com/workshops/datawrapper-oilwater6.png)

Try asking yourself another question and answer it with this dataset. Try asking questions on: 
1. A commodity besides crude oil 
2. The riskiest pipeline operators 
3. Spills in specific states

## Build the map yourself

1. Boot up [Carto.com](http://Carto.com), create a login and upload the CSV from above. 

2. Plot the data by latitude and longitude and then style the points by net barrels recovered. 

3. To add interactivity to your map, play with the "widgets" function. Add a "histogram" pulled from one of your columns, like "net_loss_barrels," and a "category" from the "iyear" column.

4. What other geographic information might be helpful? Let's add in the shapefiles for the U.S.'s crude oil pipelines. Those can be found in a [zip](https://www.eia.gov/maps/map_data/CrudeOil_Pipelines_US_EIA.zip) from the [U.S. Energy Information Administration](https://www.eia.gov/maps/layer_info-m.php). 

5. Extra points if you can track down and plot the shapefile for the Standing Rock reservation.

Read the full story on Undark [here](https://x.

![alt text](http://aleszu.com/workshops/carto-oilwater.png)

Link to Undark interactive map [here](https://undark.carto.com/viz/e053d3f2-b66b-11e6-a2ce-0e233c30368f/public_map) and workshop interactive map [here](https://storybench.carto.com/builder/eaeb6a08-0e47-11e7-a547-0ef24382571b/).

## Mapping nuclear data 

Try mapping nuclear powerplants. Data from [CarbonBrief](https://www.carbonbrief.org/mapped-the-worlds-nuclear-power-plants).

## European data 

[Shapefiles](https://www.data.gouv.fr/fr/datasets/delimitation-parcellaire-des-aoc-viticoles-de-linao/) of France's AOC regions. 

A great list from UPenn on European [GIS data](https://guides.library.upenn.edu/c.php?g=475518&p=3254771).

A shapefile of European natural gas pipelines [here](https://enipedia.org/wiki/NaturalGasInfrastructure).



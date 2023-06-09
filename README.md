# Time Sliders with Custom Date Text
This repository contains python and javascript code to set up a web map with a custom time slider that uses different labels
and date fields than the actual dates. This is intended for cases where the actual date range is not compatible
with Esri's time sliders, for example where the dates include geological time scales or dates BCE.

You can see the completed example map **[here](https://aheinlei.lsait.lsa.umich.edu/time_slider_map/time_sliders_v1.html)**.

The python code assumes the layer of interest is a feature class in an ArcGIS Pro project; similar code could be used
to update a feature layer in ArcGIS Online. Scaled date columns are added and calculated to map the original dates on to
dates ranging from 1900-2150 (or a suitable scale for your date range). The updated data is then published to ArcGIS Online,
(optionally) shared publicly, and time enabled using the newly created 
scaled date fields as the time fields. The JavaScript code illustrates how to use the original date fields to label a 
time slider based on the scaled time fields.

To use this code, do the following: 

1. Add the [Python notebook](https://gitlab.umich.edu/lsa-ts-gis-team/arcgis-large-scale-time-sliders/-/blob/main/TimeSliderSetup.ipynb) to an ArcGIS Pro project containing the feature layer of interest. 
2. Update the variables in the code as described and run the entire notebook. This will add a field or fields to your featuer layer and upload the feature layer to be shared in ArcGIS Online. It will also time-enable the online feature layer using the newly added field or fields.
3. Edit the [time_sliders_v1.html file](https://gitlab.umich.edu/lsa-ts-gis-team/arcgis-large-scale-time-sliders/-/blob/main/time_sliders_v1.html) to refer to this newly created layer, and update the variables in the html file as described for 
your use case. 
4. To publish, load the updated .html file on your server or hosting platform of choice.

#### Data Attribution
The data used in this example is a subset of the [ASCSA Corinth Excavation data](https://www.arcgis.com/home/item.html?id=f5e717c8341347a5b773d9c5e3512fdf). I'm not an archaeologist or historian and chose this dataset only for its span of date ranges, so I make no claims about the accuracy of this data--it's intended for illustration purposes only.

----
Developed by Abbey Roelofs
<br>aheinlei@umich.edu
<br>University of Michigan
<br>[](url)June 2021

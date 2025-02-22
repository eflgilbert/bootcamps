# QGIS

QGIS is an open source software for geospatial analysis and visualization. THe course I wook was available through LinkedIn Learning. It covers the following topics:
### Vector Data 
   Introduces the basic sources of data fir QGIS suck as databases, shapefiles (.shp), and WEB Feature Services (WFS). THese can all add attributes to a coordinate system.
### Raster Data
  Demonstrates use of 2-dimentional data in three forms. The first is enhanced compressed wavelet (ECW), a compace datatype file which can represent an image. Web map service (WMS) files can stream images from a remote server directly into QGIS. Finally, digital elevation model (DEM) rasters contain elevation values at each point, and can be used to create, among other things, contour maps. THe importance of matching coordinate systems between layers is emphasized int his section.
### 3D Maps
  QGIS can create 3D maps by draping an image across a DEM layer. These maps can be printed as is or converted into an animation.
  
### Other Exercises not included in this repository
- Stylizing data such as points, lines, and labels in order to make maps more readable
- Creating new datafiles from a QGIS project
- Advanced Tools (Overlay analysis, heatmaps from points, centroids from polygons)
- Using Plugins (Streetview and qgis2web)
- Python in QGIS (console and scripts)

# QGIS Raw Course Notes

Vector
- Adding vector layers as files Directories, Databases, or links

Database
  - https://lnkd.in/ga_seqg (crime reporting)
	- Shapefile (.shp) can drag and drop or browse
	- Buildings 

Shapefiles
	-Parcels, easements, Intesections, ROad centerlines
	- Keep legend order in mind for visibility


WFS WEb feature Services Data.
	- Hawaii, download APIs from hawaii.gov
- start with XYZ open streetmap zoom to hawaii
	- Maui roads https://geodata.hawaii.gov/arcgis/services/Transportation/MapServer/WFSServer?request=GetCapabilities&service=WFS
	- Kahoolawe contours 100ft
		-Lanai and Kahoolawe
	- Can query attributes from the database.


Rasters
- Open a file or link
- ECW, enhanced compressed wavelet
	- smaller datatype file
	- images can be georeferenced within the ECW file
	Make sure all the coordinate systems match up

- WMS
	- Web-based protocol that can stream images from a server to QGIS
	-Renders on the server then streams a raster image
	- Didn't change these files

- DEM - Digital elevation model
	-Raster that has elevations at each point. Can be made from LIDAR for elevation or from orthoimagery
	_Can style and blend images together by setting the greyscale ranges to be equivalent.

- Creating Contours
  Raster>Extraction>Contour

- Creating 3d Maps
	- Can use the online projection
	-Can use hidden DEM layer
	- Change the scale to observe vertical spaces in greater detail

- 3D Animations
	-After selectin animation, there is a standard pan backwards from location
	- You can set target points for whatever timestamp during the animation you want
	- Saving it outputs all of the frames
	- Recommended use Handbrake (I may use R in the future) to greate video or gif 
	- For 2D animation, just make an animation from directly above the 3D map

Styling data
-Point layers
	-Can stylize points by doing things such as changing the icon
	- IMport an svg (like clip art) as a custom icon
	- Set Unit to map units to keep the symbols the same size when zooming


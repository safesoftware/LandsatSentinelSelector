# LandsatSentinelSelector

This example provides a simple interface for the visual selection and download of
Landsat images.

The example consists of an html page and two workspaces. 

The html page landsatSelector.html uses the Leaflet.js library that shows
the map of the world. It allows panning and zooming to the required location
and specifying quality filters (% of data and cloud coverage).

A click on the map places an icon. The "Submit" button runs the first workspace,
LandsatFileSelectorWithLocation.fmw, which uses the coordinates
of the icon as parameters.

The workspace makes a path to the Landsat Amazon bucket and streams back a new 
html page with a table, which shows the previews of the images available for the 
given coordinates.The table also shows the date when the images were taken as 
well as cloud coverage information.

The previews with the location of the click shown with a red circle are made
with PreviewLocation.fmw workspace.

Clicking on the previews opens larger previews in a separate tab.

Selecting the radio button on the left from the desired preview and clicking
"Open Amazon S3 folder with selected images" button on top of the page opens
a download page with all the imagery for that tile/date.

Note that the download page is generated by the imagery provider.

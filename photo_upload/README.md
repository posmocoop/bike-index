# Photo Upload
Automated, but verified by humans


## User Story
## Before using the Photo Upload Tool (PUT)
User chooses a route of the "Velovorzugsroutennetz" (e.g. Wollishofen–Tiefenbrunnen, 7.7km) on the expert view (wrench icon) on index.velobserver.ch. He rodes along this route by taking photos. 

Minimum: 6 photos per km (more is always possible) 
Single Photo size between 3-4 MB.
EXIF data: timestamp, lat,lon of the photo

## Using the Photo Upload Tool (PUT): Upload images
In the expert view, the user can upload one or more photos per route.        
Timestamp, orig_lat, orig_lon are extracted from the image.        
           
Photos are resized and resampled (360x240) for the mobile version (Desktop version?), the original photo is kept.  
The suffix **_360x240** is added to the resized and resampled image.        

Photos are positioned via pins on the edge. We keep orig_lon, orig_lat and then project and position pins on the route (pin_lon, pin_lat). Pins can only be moved along the route.   

## Positioning a pin, verifying and editing, saving text  

If you click the pin, you see the photo and a "Verify"-Button underneath. If you click "Verify", the pin is fixed and the photo becomes available on index.velobserver.ch. The following data is shown and remains editable (Edit/Save Button). 

- timestamp as DD.MM.YYYY, HH:MM, e.g. 19.1.2022, 15:20 (**not** editable)
- pin_lat, pin_lon (**not** editable)
- edge_id (**not** editable)
- street_name (editable)
- (street_number)
- (neighborhood?)
- city (**not** editable)
- country, Alpha-2 ISO-Code, e.g. CH, "Zürich, CH", "Berlin, DE", "Paris, FR" (not editable)

## Constraints
- One image per edge (?) - so that we do not have an old image and a new image after infrastructure changes
- Always the newest photo is shown on index

## On index.velobserver.ch
The bbox of the map is centered on the pin, the full edge is shown


## Tools
- imagemagick (rokka?)









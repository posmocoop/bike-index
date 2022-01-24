# Photo Upload


## Revised User Story
1. In the expert view, the user A uploads photos with EXIF data for a *given route* (route Wollishofen – Tiefenbrunnen). E.g. it would be good to give them an id (eg. there will probably be 2 routes Wollishofen - Tiefenbrunnen and Tiefenbrunnen - Wollishofen, the second one gets an "R" for direction).  
(EXIF data, timestamp, lat, lon is extracted). After that a csv download of the data is available for the route. 

2. User B (or user A) populates the csv. Then the database is updated, either via pgadmin or via expert view. 




## User Story 
Automated, but verified by humans

## 1. Before using the Photo Upload Tool (PUT)
User chooses a route of the "Velovorzugsroutennetz" (e.g. Wollishofen–Tiefenbrunnen, 7.7km) on the expert view (wrench icon) on index.velobserver.ch. 
S/He rodes along this route by taking photos. 

Minimum: 6 photos per km (more is always possible)    
Single Photo size between 3-4 MB.               
EXIF data: timestamp, lat,lon of the photo              

## 2. Using the Photo Upload Tool (PUT): Upload images
In the expert view, the user can upload one or more photos per route.        
Timestamp, orig_lat, orig_lon are extracted from the image.          
               
Photos are resized and resampled (360x240) for the mobile version (Desktop version?), the original photo is kept.  
The suffix "_360x240" is added to the resized and resampled image.                    
            
Photos are positioned via pins on the edge. We keep orig_lon, orig_lat and then project and position pins on the route (pin_lon, pin_lat). Pins can only be moved along the route.        

### Upload 
By clicking (Upload Photos) one can find and select one or more pictures to upload. Pictures can be uploaded in sequence. 

### After Upload
```
Photos | Verified                 
77     | 16       
```   

### Verified pin color
Verified pins are green, not verified pins are red


## Positioning a pin, verifying and editing, saving text  

If you click the pin, you see the photo, text and a "Verify"-Button underneath. If you click "Verify", the pin is fixed and the photo becomes available as a photo on index.velobserver.ch. The following data is shown under the picture and remains editable (Edit/Save Button), similar in design as for the rating. 
```
[PHOTO]
          
(Edit | Save)            
street_name, neighborhood                   timestamp
city, country_code

(Verify)
```

**In DB**: 
- path to photo 360x240
- path to original
- timestamp as ISO date/time with local offset (e.g. YYYY-MM-DDTHH:MM+01:00), displayed as DD.MM.YYYY, HH:MM, e.g. 19.1.2022, 15:20 (**not** editable)
- lat, lon
- pin_lat, pin_lon (**not** editable)
- edge_id (**not** editable)
- street_name (editable)
- (street_number)
- (neighborhood?)
- city (**not** editable)
- country_code, Alpha-2 ISO-Code, e.g. CH, "Zürich, CH", "Berlin, DE", "Paris, FR" (not editable)

### Verified pin color
Verified pins are green, not verified pins are red


## Constraints
- One image per edge (?) - so that we do not have an old image and a new image after infrastructure changes
- Always the newest photo is shown on index

## On index.velobserver.ch
The bbox of the map is centered on the pin, the full edge is shown


## Tools
- imagemagick (rokka?)









# Photo Upload


## Revised User Story

### Upload of photos
In the expert view, the user A uploads photos with EXIF data for a *given route* (route Wollishofen – Tiefenbrunnen). 
(EXIF data, timestamp, lat, lon is extracted). After that a csv download of the data is available for the route. 


### Table Routes (network_routes)
- route_id
- route_name (e.g. Wollishofen - Tiefenbrunnen)
- default (1 for default, 0 otherwise)
- direction (I for inbound, O for outbound) 

An edge can have multiple directions.
                       
See also: https://github.com/posmocoop/veloplan#edges                   
And, p.48: http://www.normes-donnees-tc.org/wp-content/uploads/2017/01/TC_278_WI_00278420_E-RS-170118-final3.pdf

### Table Photos (network_route_edges_images)
- **id**
- **route_id** (optional)
- **network_ogc_fid** (=edge id)
- **image_filename** 
- **image_url** (=original path, not imgix path)
- **exif_datetime** (as ISO 8601, local: YYYY-MM-DDTHH:MM+01:00 = local time)
- **exif_lat**
- **exif_lon**
- **pin_lat** (= lat, lon, positioned on the edge)
- **pin_lon** 
- **street_name**
- **street_number** (optional)
- **neighborhood** (optional)
- **city**
- **geoid** (75601120261 for Zurich, important for a multilingual site)
- **country_code** (Alpha-2 ISO-Code)  
- **created_at**
- **update_at**
- **deleted_at**

**NOTE:** 
City, country_code will be displayed as "Zürich, CH", "Berlin, DE", "Paris, FR" (not editable)                   
Exif_datetime will be displayed as "DD.MM.YYYY, HH:MM", zeroes are stripped

### Update of the database
User B (or user A) populates the csv. Then the database is updated, either via pgadmin or via expert view. 




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
imgix = has the advantage that the images remain with us
- imagemagick or rokka?)









# Traffic video 

## State Template
### Site Template

-- FPS: 
-- Resolution: 
-- Can Download:  

## Texas
 * Site:
--  FPS: 1 frame per 3:30
-- Resolution: Low
-- Can Download: False
I believe there's some state laws limiting the footage of traffic cams. What ever it is, it makes traffic footage useless.

## Florida 
* https://fl511.com/#Camera
-- FPS:24ish? maybe 30?
-- Resolution: 800x450 (2 sample), 1280x720 (1 sample)
-- Can Download:  True
Remarks: Florida has at least some live-feeds. They also have sunshine laws which might not directly help in this instances, but it means records are more accessible. I think they're our best bet for now.

## California 
### # Caltrans
* URL: http://cwwp2.dot.ca.gov/vm/iframemap.htm
* URL: https://cwwp2.dot.ca.gov/
* URL: https://cwwp2.dot.ca.gov/vm/streamlist.htm 
--  FPS:  15 (1 sample)
-- Resolution: (320x240)
-- Can Download: True
-- ToS: https://dot.ca.gov/conditions-of-use
 Remarks: Cali is the best option for video footage so long as we can find reports. We can book mark streams. We can get a list of them. We can look at a map. The only issues are the lack of search in map, multiple cameras sending corrupt streams, and possible legal requirements. 

## Washington
### Washington State Department of Transportation
* http://wsdot.com/Travel/Real-time/Map/?featuretype=camera&featureid=10125
--  FPS: 1 frame per 5 minutes
-- Resolution:  335x250
-- Can Download: ???  
I thought Washington would have real time traffic cams. Bust! 
### King5 - News 
 * https://www.king5.com/traffic-cameras
--  FPS:  ???
-- Resolution: ??? 
-- Can Download: False  
It's just showing a nearly blank page for me. Maybe a dead link or site. Maybe you need to be in Washington to access it?
## Maryland 
### Maryland **Chart / Department of Transportation**
* https://chart.maryland.gov/TrafficCameras/GetTrafficCameras
--  FPS: 15
-- Resolution: 352x240
-- Can Download: True  
Google messed up and gave me the wrong state's site. Turns out it's a nice traffic cam site. You can tell they took it seriously and paid some real tax payer dollars on the sites back end. They likely took the funds from the camera fun it, but it's acceptable quality. 
# Accident reports 
## Template state
### Template site
* 
-- Data Fields:

## Florida
### ★Florida Highway Safety Motor Vehicle★
* https://www.flhsmv.gov/fhp/traffic/live_traffic_feed.html
* Data Fields: `Incident Type`, `Dispatch time` in military time, `Arrival time` in military time, `county`, `location`, `remarks` 
I have no problem with scraping this data. It seems reasonable data set with a focus on highway/freeway/interstate which have better traffic cam coverage. 
### Florida 511
* https://fl511.com/list/events/traffic?start=0&length=25&filters%5B0%5D%5Bi%5D=5&filters%5B0%5D%5Bs%5D=Incidents&order%5Bi%5D=2&order%5Bdir%5D=asc
* Data Fields: `Region`, `County`, `Roadway`, `Direction`, `Type`, `Severity`, `Description`, `Start Time` in MM/DD/YY HH:MM:SS AM/PM, `Last Updated` in MM/DD/YY HH:MM:SS AM/PM, `Camera Image`
I'm not bullish on this source. It seems more residential which i'd rather avoid. The camera Image is just that, a image, and tends to not show anything if i accident happens. 
### Open data (Florida)
* https://gis-fdot.opendata.arcgis.com/
* Data Fields: This is a data base of reports and statistics which are years out of date.
Not really helpful at this stage, but if we attempt to scale up to multiple locations, having information like this might help find high incident areas.  
### Sarasota County - Dispatch Reporting 
* https://dispatchreporting.scgov.net/Events?strAgencyID=All
* Data Fields: `EventDate` in MM/DD/YY, `Time` in military, `Event` `Location` `Grid` `Zone` `Case#` `Event#`
* Oddity: Events will have multiple entries with the only change being `Case#` 
This seems like a lot of local roads. There's also the added requirement to filter out duplicate entries. I'd avoid this for the time being, but it's also most exactly what i'd want.  
## Maryland
Data Montgomery County 
* https://data.montgomerycountymd.gov/Public-Safety/Police-Dispatched-Incidents/98cc-bc7d/about_data
* Data Fields: Some CVS file
 Maybe useful, but it's a CVS file that gets updated 4 times a day. 
###  Data Montgomery County 
* https://data.montgomerycountymd.gov/Public-Safety/Police-Dispatched-Incidents/98cc-bc7d/about_data
* https://data.montgomerycountymd.gov/Public-Safety/MC-Police-Dispatched-Incidents-Map/m9j8-ehy3
* Data Fields: Some CVS file
Maybe useful, but it's a CVS file that gets updated 4 times a day. 
## California 
### Weather Share
* https://oss.weathershare.org/?clat=37.81998&clng=-122.31338&zoom=12
* Data Fields:
This is just a traffic map which covers Washington to New Mexico. It contains still images from Traffic cams in all states in that box area, along with accidents markers. I **haven't** been able to cross reference an incident with a traffic cam yet.  
### California Highway Patrol
* http://chp.ca.gov/traffic
* Data Fields: `No.`, `Time` in HH:MM AM/PM, `Type`, `Location`, `Location Desc`, `Area`, and `Details + Units`
 It does provide additional information if you hit details, but the data isn't easy enough to parse for location camera location.
### San Diego Police Dispatch
* https://webapps.sandiego.gov/sdpdonline
* Data Fields: `Call DateTime` in YYYY-MM-DD HH:MM:SS military, `Call Type`, `Division`, `Nighborhood`  
**Useless!** 
# concept
home = house/apartment
- distance
  - display homes within X miles of {location}
- density
  - display homes with at least X {location} within distance
- nearby
  - display number of {location} within X distance


## resources needed

### homes apis
- zillow
  - houses
  - apartments
- apartments.com
- (other?)

### google maps apis
- places api
- distance matrix API


## solution

### distance
- for home in homes
  - if not nearby(location) remove home from homes

### density
- for home in homes
  - if responses for nearby(location) less than densityRequirement remove home from homes

#### nearby 
- convert home address to latlong
- request 
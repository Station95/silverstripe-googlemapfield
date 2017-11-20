silverstripe-googlemapfield
==============

Lets you record a precise location using latitude/longitude/zoom fields to a DataObject.

Displays a map using the Google Maps API. The user may then choose where to place the marker; the landing coordinates are then saved.

You can also search for locations using the search box, which uses the Google Maps Geocoding API.

### Usage

##### `__construct` options

|Option|Default|Description|
|------|-------|-----------|
|`field_names`|See `GoogleMapField.yml`'s `default_options.field_names`|A map of field names to save the map data into your object.|

##### make sure `api_key` config added in site yml file
```yml
BetterBrief\GoogleMapField\GoogleMapField:
  default_options:
    api_key: 'GOOGLE_API_KEY'
```

##### `Field` options

|Option|Default|Description|
|------|-------|-----------|
|`coords`|Your object's latitude and longitude|The intial coordinates of the map - note: this is not the default value if no object exists|
|`map`|Zoom of 14, map type of ROADMAP|A [google.maps.MapOptions](https://developers.google.com/maps/documentation/javascript/reference?csw=1#MapOptions) object|

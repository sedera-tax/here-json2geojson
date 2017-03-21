# HERE JSON to GeoJSON

JavaScript library to transform HERE JSON objects to GeoJSON.

[![Build Status](https://travis-ci.org/meggsimum/here-json2geojson.svg?branch=master)](https://travis-ci.org/meggsimum/here-json2geojson)
[![dependencies Status](https://david-dm.org/meggsimum/here-json2geojson/status.svg)](https://david-dm.org/meggsimum/here-json2geojson)
[![devDependencies Status](https://david-dm.org/meggsimum/here-json2geojson/dev-status.svg)](https://david-dm.org/meggsimum/here-json2geojson?type=dev)

At the moment only a subset of the JSON response types provided by the [HERE REST APIs](https://developer.here.com/api-explorer/rest) is supported. This will be extended from time to time.

#### Disclaimer

**This is not an official HERE product!**

Be sure to respect the [HERE Service Terms](https://legal.here.com/en/terms/serviceterms/us/) when using their API.

## Usage

To use this library in an HTML-web-application just include the JavaScript-file at `dist/hj2gj.js` into your HTML-page. Otherwise just import this library as module like in the snippet below:

```JavaScript
import {readIsolines} from 'here-json2geojson';

var hereIsolineResponse = // The response of the HERE REST API call
var isolineFeatColl = readIsolines(hereIsolineResponse);
```

### Build the library on your own

    > npm install
    > npm run dist

Afterwards the single-file-build of the library is available under `dist/hj2gj.js`

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### readRoute

Reads route-response object delivered by the HERE API and converts it
to a GeoJSON FeatureCollection holding the route legs as line features.

**Parameters**

-   `hereRouteResponse` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** HERE JSON for a route

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** GeoJSON FeatureCollection

### readWeatherConditions

Reads HERE traffic weather conditions and transforms them to a GeoJSON
FeatureCollection containing point features with weather info as attributes.

**Parameters**

-   `weatherConditionsResponse` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** HERE JSON for weather conditions

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** GeoJSON FeatureCollection

### readPlaces

Reads places-response object delivered by the HERE API and converts it
to a GeoJSON FeatureCollection holding the places as point features.

**Parameters**

-   `herePlacesResponse` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** HERE JSON for a place

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** GeoJSON FeatureCollection

### readTrafficIncidents

Reads HERE traffic incidents and transforms them to a GeoJSON
FeatureCollection containing point features.

**Parameters**

-   `trafficIncidentsResponse` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** HERE JSON for traffic incidents
-   `addEndPoints` **[Boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** Should possible end points of incident be added to the FeatureCollection

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** GeoJSON FeatureCollection

### readIsolines

Reads isolines-response object delivered by the HERE API and converts it
to a GeoJSON FeatureCollection.

**Parameters**

-   `hereIsolineResponse` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** HERE JSON for isolines

Returns **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** GeoJSON FeatureCollection

## Credits

The initial development of this project has been sponsored by [geomer GmbH](http://geomer.de/) from Heidelberg, Germany

# Cloudmade Lib

A node library for consuming Cloudmade APIs. Currently only supports Geocoding.

[![Build Status](https://travis-ci.org/PlayNetwork/cloudmade-lib.png?branch=develop)](https://travis-ci.org/PlayNetwork/cloudmade-lib) [![Coverage Status](https://coveralls.io/repos/PlayNetwork/cloudmade-lib/badge.png?branch=develop)](https://coveralls.io/r/PlayNetwork/cloudmade-lib?branch=develop)

## Features

* Geocoding
	* Output types for JSON, GeoJSON, Property list and HTML

## Install

This module is currently under development and has not been published to NPM yet.

```Bash
npm install cloudmade-lib
```

## Usage

### Get JSON

To retrieve results in JSON format, see the following example:

```Javascript
var
	cloudmade = require('cloudmade'),
	geocoding = cloudmade.geocoding.initialize({
		apikey : 'your_api_key_here'
	});

geocoding.get('8727 148th Ave NE, Redmond, WA 98052', function (err, data) {
	// work with results here...
});
```

### Optional Parameters

<http://developers.cloudmade.com/projects/show/geocoding-http-api#Parameters>


### Response Data

```JSON
{
	"apikey" : "your_api_key_here",
	"data" : {},
	"host" : "geocoding.cloudmade.com",
	"path" : "/geocoding/v2/find.js",
	"query" : "?query=8727%20148th%20Ave%20NE%2C%20Redmond%2C%20WA%2098052",
	"secure" : false
}
```

## License

MIT, see LICENSE
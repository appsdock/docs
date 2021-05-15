# App REST API

This page provides a list of all app REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## The app resource

### Attributes

**id** `string`


**name** `string`


**active** `bool`


**version** `string`


**build** `string`


**status** `string`


**channel** `string`


### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": "My app",
    "active": true,
    "version": "1.0.0",
    "build": "xy-123 (2000-01-01)",
    "status": "READY",
    "channel": "BETA"
}
~~~

## Activate an app

### Parameters

This endpoint has no parameters.

## Deactivate an app

### Parameters

This endpoint has no parameters.

## Install an app

### Parameters

This endpoint has no parameters.

## List all apps

### Parameters

This endpoint has no parameters.

## Uninstall an app

### Parameters

This endpoint has no parameters.

## Update an app

### Parameters

This endpoint has no parameters.


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

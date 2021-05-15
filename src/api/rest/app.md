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
{\n\t"id":"680fe5ff-3b68-4d22-bb91-eb6a9712f78d",\n\t"name":"My app",\n\t"active":true,\n\t"version":"1.0.0",\n\t"build":"xy-123 (2000-01-01)",\n\t"status":"READY",\n\t"channel":"BETA"\n}
~~~

## Activate an app

## Deactivate an app

## Install an app

## List all apps

## Uninstall an app

## Update an app


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

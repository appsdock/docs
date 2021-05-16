# App REST API

This page provides a list of all app REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## App

### Resource

#### Attributes

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The app ID in UUID format.
| **name** | `string` | The name of the application.
| **active** | `bool` | The activity status of the application.
| **version** | `string` | The version number of the application. The number is divided into major, minor and revision number, each separated by a dot.
| **build** | `string` | The build number of the application. The number can be freely assigned.
| **status** | `string` | The life status of the application.
| **channel** | `string` | The development status of the application.

#### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": "Jarvis",
    "active": true,
    "version": "1.0.0",
    "build": "#59-1964",
    "status": "READY",
    "channel": "BETA"
}
~~~

### Requests

### Activate an app

`POST` **/v1/apps:activate/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### Deactivate an app

`POST` **/v1/apps:deactivate/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### Install an app

`POST` **/v1/apps:install/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### List all apps

`GET` **/v1/apps**

#### Parameters

!!! important "This endpoint has no parameters."

### Uninstall an app

`POST` **/v1/apps:uninstall/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### Update an app

`POST` **/v1/apps:update/{id}**

#### Parameters

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

[^1]: Yes
[^2]: No

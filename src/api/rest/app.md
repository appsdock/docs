# App Resources

This page provides a list of all app resource endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## App

### The App resource
~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": "Jarvis",
    "active": true,
    "version": "1.0.0",
    "status": "READY"
}
~~~

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The app ID in UUID format.
| **name** | `string` | The name of the application.
| **active** | `bool` | The activity status of the application.
| **version** | `string` | The version number of the application. The number is divided into major, minor and revision number, each separated by a dot.
| **status** | `string` | The life status of the application.


### Activate an app

`POST` **/v1/apps:activate/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### Deactivate an app

`POST` **/v1/apps:deactivate/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### Install an app

`POST` **/v1/apps:install/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### List all apps

`GET` **/v1/apps**


**Parameters**

!!! important "This endpoint has no parameters."

### Uninstall an app

`POST` **/v1/apps:uninstall/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### Update an app

`POST` **/v1/apps:update/{id}**


**Parameters**

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[ID]: Identifier
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

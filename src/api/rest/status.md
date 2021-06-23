# Status Resources

This page provides a list of all organization resource endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Status

### The Status resource
~~~json
{
    "API-Server": "OK"
}
~~~

| Attribute | Type | Description
| --------- | ---- | -----------
| **API-Server** | `string` | Shows the API status.


### Shows the system status.

`GET` **/v1/status**


**Parameters**

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

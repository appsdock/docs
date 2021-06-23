# Status REST API

This page provides a list of all organization REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Status

### Resource

~~~json
{
    "API-Server": "OK"
}
~~~

| Attribute | Type | Description
| --------- | ---- | -----------
| **API-Server** | `string` | Shows the API status.

### Endpoints

#### Shows the system status.

`GET` **/v1/status**

##### Parameters

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

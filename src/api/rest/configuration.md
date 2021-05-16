# Configuration REST API

This page provides a list of all configuration REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## The setting resource

### Attributes

| Attribute | Type | Description
| --------- | :--: | -----------
| **id** | `string` | 
| **type** | `string` | 
| **value** | `array`\|`null` | 
| **default** | `array`\|`null` | 
| **options** | `array`\|`null` | 

### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "type": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "value": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "default": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "options": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d"
}
~~~

## Change a configuration setting

`POST` **/v1/settings/{id}**

### Parameters

| Parameter | Type | Required | Description
| --------- | :--: | :------: | -----------
| **value** | `bool`\|`int`\|`string`\|`array` | ❌ | Value of the configuration setting.

### Payload

~~~json
{
    "value": "Europe\/Berlin"
}
~~~

## Get a configuration setting

`GET` **/v1/settings/{id}**

### Parameters

!!! important "This endpoint has no parameters."

## List all configuration settings

`GET` **/v1/settings**

### Parameters

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

*[✓]: Yes
*[❌]: No

# Configuration Resources

This page provides a list of all configuration resource endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Setting

### The Setting resource
~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "type": "STRING",
    "value": [
        "America\/New_York"
    ],
    "default": [
        "Europe\/Berlin"
    ],
    "options": null
}
~~~

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The setting ID as UUID.
| **type** | `string` | The data type of the setting.
| **value** | `array` \| `null` | The value of the setting.
| **default** | `array` \| `null` | The default value of the setting.
| **options** | `array` \| `null` | The options of the setting.


### Change a configuration setting

`POST` **/v1/settings/{id}**

!!! info "Description"
    Changes the value of the setting resource.


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **value** | `bool` \| `int` \| `string` \| `array` | ✔ | The value of the setting. The type of value depends on the specified data type.

##### Payload

~~~json
{
    "value": "Europe\/Berlin"
}
~~~

### Get a configuration setting

`GET` **/v1/settings/{id}**

!!! info "Description"
    Returns the setting resource.


**Parameters**

!!! important "This endpoint has no parameters."

### List all configuration settings

`GET` **/v1/settings**

!!! info "Description"
    Returns a collection of all setting resources.


**Parameters**

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[ID]: Identifier
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

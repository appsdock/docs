# Identity REST API

This page provides a list of all identity REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## The group resource

### Attributes

**id** `string`
The identifier of the group as UUID.

**name** `array`
Name of the group in one or more languages.

**createdBy** `string`


**createdAt** `int`


### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    },
    "createdBy": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "createdAt": 1620979351
}
~~~

## Assign a user to a group.

### Parameters

This endpoint has no parameters.

## Create a group

### Parameters

**name** `array` optional

### Payload

~~~json
{
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    }
}
~~~

## Delete a group

### Parameters

This endpoint has no parameters.

## Get a group

### Parameters

This endpoint has no parameters.

## List all groups

### Parameters

This endpoint has no parameters.

## Remove a user from a group.

### Parameters

This endpoint has no parameters.

## Rename a group

### Parameters

**name** `array` optional

### Payload

~~~json
{
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    }
}
~~~
## The role resource

### Attributes

**id** `string`
The identifier of the role as UUID.

**name** `array`
Name of the role in one or more languages.

**type** `string`


**isPredefined** `bool`


### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    },
    "type": "USER",
    "isPredefined": true
}
~~~

## Assign a role to a group

### Parameters

This endpoint has no parameters.

## Assign a role to a user

### Parameters

This endpoint has no parameters.

## Create a role

### Parameters

**name** `array` optional

**type** `string` optional
Type of the role.

### Payload

~~~json
{
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    },
    "type": "USER"
}
~~~

## Delete a role

### Parameters

This endpoint has no parameters.

## Get a role

### Parameters

This endpoint has no parameters.

## List all roles

### Parameters

This endpoint has no parameters.

## Remove a role from a group

### Parameters

This endpoint has no parameters.

## Remove a role from a user

### Parameters

This endpoint has no parameters.

## Rename a role

### Parameters

**name** `array` optional

### Payload

~~~json
{
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    }
}
~~~
## The user resource

### Attributes

**id** `string`
The identifier of the user as UUID.

**username** `string`
The username of the user.

**email** `string`
The email address of the user.

**name** `string`
The name of the user.

**status** `string`
The current status of the user.

**verified** `bool`
Shows if the user is verified.

**penultimateLoginAt** `int`


**createdAt** `int`
Timestamp of the record creation.

### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "username": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "email": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "status": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "verified": true,
    "penultimateLoginAt": 1620979351,
    "createdAt": 1620979351
}
~~~

## Create a user

### Parameters

**organizationId** `string` optional

**username** `string` optional

**password** `string` optional

**email** `string` optional

**name** `string` optional

**roles** `array` optional
The roles which should be assigned to the user as UUID.

### Payload

~~~json
{
    "organizationId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "username": "IronMan",
    "password": "4-v3ry.53cr37_p455w0rd",
    "email": "tony@stark-industries.com",
    "name": "Tony Stark",
    "roles": [
        "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
        "680fe5ff-3b68-4d22-bb91-eb6a9712f78d"
    ]
}
~~~

## Delete a preference for a user.

### Parameters

This endpoint has no parameters.

## Get a user

### Parameters

This endpoint has no parameters.

## Get a user identity

### Parameters

This endpoint has no parameters.

## List all users

### Parameters

This endpoint has no parameters.

## Get the current user

### Parameters

This endpoint has no parameters.

## Get the current user policies

### Parameters

This endpoint has no parameters.

## Get the current user preferences

### Parameters

This endpoint has no parameters.

## Set the password for a user

### Parameters

**password** `string` optional
The password of the user.

**securityToken** `string` optional
The security token to authenticate.

### Payload

~~~json
{
    "password": "4-v3ry.53cr37_p455w0rd",
    "securityToken": "4-v3ry.53cr37_p455w0rd"
}
~~~

## Set a preference for a user

### Parameters

**settingId** `string` optional
The ID of the configuration setting.

**value** `bool|int|string|array` optional
The value to set the configuration setting set to.

### Payload

~~~json
{
    "settingId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "value": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    }
}
~~~


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

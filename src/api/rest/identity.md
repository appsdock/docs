# Identity REST API

This page provides a list of all identity REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Group

### Resource

#### Attributes

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The identifier of the group as UUID.
| **name** | `array` | Name of the group in one or more languages.
| **createdBy** | `string` | 
| **createdAt** | `int` | 

#### Response

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

### Requests

### Assign a user to a group.

`POST` **/v1/groups/{groupId}/users/{userId}**

#### Parameters

!!! important "This endpoint has no parameters."

### Create a group

`POST` **/v1/groups**

#### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✓[^1] | Name of the group in one or more languages.

#### Payload

~~~json
{
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    }
}
~~~

### Delete a group

`DELETE` **/v1/groups/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### Get a group

`GET` **/v1/groups/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### List all groups

`GET` **/v1/groups**

#### Parameters

!!! important "This endpoint has no parameters."

### Remove a user from a group.

`DELETE` **/v1/groups/{groupId}/users/{userId}**

#### Parameters

!!! important "This endpoint has no parameters."

### Rename a group

`PATCH` **/v1/groups/{id}**

#### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✓[^1] | Name of the group in one or more languages.

#### Payload

~~~json
{
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    }
}
~~~
## Role

### Resource

#### Attributes

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The identifier of the role as UUID.
| **name** | `array` | Name of the role in one or more languages.
| **type** | `string` | 
| **isPredefined** | `bool` | 

#### Response

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

### Requests

### Assign a role to a group

`POST` **/v1/roles/{roleId}/groups/{groupId}**

#### Parameters

!!! important "This endpoint has no parameters."

### Assign a role to a user

`POST` **/v1/roles/{roleId}/users/{userId}**

#### Parameters

!!! important "This endpoint has no parameters."

### Create a role

`POST` **/v1/roles**

#### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✓[^1] | Name of the role in one or more languages.
| **type** | `string` | ✓[^1] | Type of the role.

#### Payload

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

### Delete a role

`DELETE` **/v1/roles/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### Get a role

`GET` **/v1/roles/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### List all roles

`GET` **/v1/roles**

#### Parameters

!!! important "This endpoint has no parameters."

### Remove a role from a group

`DELETE` **/v1/roles/{roleId}/groups/{groupId}**

#### Parameters

!!! important "This endpoint has no parameters."

### Remove a role from a user

`DELETE` **/v1/roles/{roleId}/users/{userId}**

#### Parameters

!!! important "This endpoint has no parameters."

### Rename a role

`PATCH` **/v1/roles/{id}**

#### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✓[^1] | Name of the role in one or more languages.

#### Payload

~~~json
{
    "name": {
        "de-DE": "Entwicklung",
        "en-GB": "Development",
        "zh-Hans-HK": "\u53d1\u5c55"
    }
}
~~~
## User

### Resource

#### Attributes

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The identifier of the user as UUID.
| **username** | `string` | The username of the user.
| **email** | `string` | The email address of the user.
| **name** | `string` | The name of the user.
| **status** | `string` | The current status of the user.
| **verified** | `bool` | Shows if the user is verified.
| **penultimateLoginAt** | `int` | 
| **createdAt** | `int` | Timestamp of the record creation.

#### Response

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

### Requests

### Create a user

`POST` **/v1/users**

#### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **organizationId** | `string` | ❌[^2] | The identifier of the user as UUID.
| **username** | `string` | ✓[^1] | The username of the user.
| **password** | `string` | ✓[^1] | The password of the user.
| **email** | `string` | ✓[^1] | The email address of the user.
| **name** | `string` | ✓[^1] | The name of the user.
| **roles** | `array` | ❌[^2] | The roles which should be assigned to the user as UUID.

#### Payload

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

### Delete a preference for a user.

`DELETE` **/v1/users/me/preferences/{settingId}**

#### Parameters

!!! important "This endpoint has no parameters."

### Get a user

`GET` **/v1/users/{id}**

#### Parameters

!!! important "This endpoint has no parameters."

### Get a user identity

`GET` **/v1/users/{id}/identity/{securityToken}**

#### Parameters

!!! important "This endpoint has no parameters."

### List all users

`GET` **/v1/users**

#### Parameters

!!! important "This endpoint has no parameters."

### Get the current user

`GET` **/v1/users/me**

#### Parameters

!!! important "This endpoint has no parameters."

### Get the current user policies

`GET` **/v1/users/me/policies**

#### Parameters

!!! important "This endpoint has no parameters."

### Get the current user preferences

`GET` **/v1/users/me/preferences**

#### Parameters

!!! important "This endpoint has no parameters."

### Set the password for a user

`PATCH` **/v1/users/{id}/password**

#### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **password** | `string` | ✓[^1] | The password of the user.
| **securityToken** | `string` | ✓[^1] | The security token to authenticate.

#### Payload

~~~json
{
    "password": "4-v3ry.53cr37_p455w0rd",
    "securityToken": "4-v3ry.53cr37_p455w0rd"
}
~~~

### Set a preference for a user

`PUT` **/v1/users/me/preferences**

#### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **settingId** | `string` | ✓[^1] | The ID of the configuration setting.
| **value** | `bool` \| `int` \| `string` \| `array` | ✓[^1] | The value to set the configuration setting set to.

#### Payload

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
*[UUID]: Universally Unique Identifier

[^1]: Yes
[^2]: No

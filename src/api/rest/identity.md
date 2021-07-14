# Identity Resources

This page provides a list of all identity resource endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Group

### The Group resource
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

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The ID of the group as UUID.
| **name** | `array` | The name of the group per language.
| **createdBy** | `string` | The ID of the user who created the group as UUID.
| **createdAt** | `int` | The time of creation ot the record as a timestamp.


### Assign a user to a group

`POST` **/v1/groups/{groupId}/users/{userId}**


**Parameters**

!!! important "This endpoint has no parameters."

### Create a group

`POST` **/v1/groups**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✔ | The name of the group per language.

##### Payload

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


**Parameters**

!!! important "This endpoint has no parameters."

### Get a group

`GET` **/v1/groups/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### List all groups

`GET` **/v1/groups**


**Parameters**

!!! important "This endpoint has no parameters."

### Remove a user from a group

`DELETE` **/v1/groups/{groupId}/users/{userId}**


**Parameters**

!!! important "This endpoint has no parameters."

### Rename a group

`PATCH` **/v1/groups/{id}**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✔ | The name of the group per language.

##### Payload

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

### The Role resource
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

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The ID of the role as UUID
| **name** | `array` | The name of the role per language.
| **type** | `string` | The type of the role. Valid values are: USER, ADMIN, GUEST, EXTERNAL
| **isPredefined** | `bool` | Shows if the role is predefined or a created by a user.


### Assign a role to a group

`POST` **/v1/roles/{roleId}/groups/{groupId}**


**Parameters**

!!! important "This endpoint has no parameters."

### Assign a role to a user

`POST` **/v1/roles/{roleId}/users/{userId}**


**Parameters**

!!! important "This endpoint has no parameters."

### Create a role

`POST` **/v1/roles**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✔ | The name of the role per language.
| **type** | `string` | ✔ | Type of the role. Valid values are: USER, ADMIN, GUEST, EXTERNAL

##### Payload

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


**Parameters**

!!! important "This endpoint has no parameters."

### Get a role

`GET` **/v1/roles/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### List all roles

`GET` **/v1/roles**


**Parameters**

!!! important "This endpoint has no parameters."

### Remove a role from a group

`DELETE` **/v1/roles/{roleId}/groups/{groupId}**


**Parameters**

!!! important "This endpoint has no parameters."

### Remove a role from a user

`DELETE` **/v1/roles/{roleId}/users/{userId}**


**Parameters**

!!! important "This endpoint has no parameters."

### Rename a role

`PATCH` **/v1/roles/{id}**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `array` | ✔ | The name of the role per language.

##### Payload

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

### The User resource
~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "username": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "email": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "status": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "penultimateLoginAt": 1620979351,
    "createdAt": 1620972963
}
~~~

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The ID of the user as UUID.
| **username** | `string` | The username of the user.
| **email** | `string` | The email address of the user.
| **name** | `string` | The name of the user.
| **status** | `string` | The life status of the user.
| **penultimateLoginAt** | `int` | The penultimate login of the user as a timestamp.
| **createdAt** | `int` | The time of creation ot the record as a timestamp.


### Create a user

`POST` **/v1/users**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **organizationId** | `string` | ✖ | The ID of the organization as UUID.
| **username** | `string` | ✔ | The username of the user.
| **password** | `string` | ✖ | The password of the user.
| **email** | `string` | ✔ | The email address of the user.
| **name** | `string` | ✔ | The name of the user.
| **roles** | `array` | ✖ | The ID of the role as UUID which should be assigned to the user.

##### Payload

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

### Delete a user preference

`DELETE` **/v1/users/me/preferences/{settingId}**


**Parameters**

!!! important "This endpoint has no parameters."

### Get a user

`GET` **/v1/users/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### Get a user identity

`GET` **/v1/users/st-{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### List all users

`GET` **/v1/users**


**Parameters**

!!! important "This endpoint has no parameters."

### Resend the registration complete mail.

`POST` **/v1/users/{id}/mails/completeRegistration**


**Parameters**

!!! important "This endpoint has no parameters."

### Get the current user

`GET` **/v1/users/me**


**Parameters**

!!! important "This endpoint has no parameters."

### Get the current user policies

`GET` **/v1/users/me/policies**


**Parameters**

!!! important "This endpoint has no parameters."

### Get the current user preferences

`GET` **/v1/users/me/preferences**


**Parameters**

!!! important "This endpoint has no parameters."

### Get the current user roles

`GET` **/v1/users/me/roles**


**Parameters**

!!! important "This endpoint has no parameters."

### Set a user password

`PATCH` **/v1/users/{id}/password**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **password** | `string` | ✔ | The password of the user.
| **securityToken** | `string` | ✔ | The security token to authenticate.

##### Payload

~~~json
{
    "password": "4-v3ry.53cr37_p455w0rd",
    "securityToken": "4-v3ry.53cr37_p455w0rd"
}
~~~

### Set a user preference

`PUT` **/v1/users/me/preferences**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **settingId** | `string` | ✔ | The ID of the configuration setting.
| **value** | `bool` \| `int` \| `string` \| `array` | ✔ | The value to set the configuration setting set to.

##### Payload

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

### Update a user

`PATCH` **/v1/users/{id}**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **username** | `string` | ✖ | The username of the user.
| **password** | `string` | ✖ | The password of the user.
| **email** | `string` | ✖ | The email address of the user.
| **name** | `string` | ✖ | The name of the user.

##### Payload

~~~json
{
    "username": "IronMan",
    "password": "4-v3ry.53cr37_p455w0rd",
    "email": "tony@stark-industries.com",
    "name": "Tony Stark"
}
~~~


*[API]: Application Programming Interface
*[ID]: Identifier
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

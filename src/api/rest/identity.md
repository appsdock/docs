# Identity REST API

This page provides a list of all identity REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Assign a user to a group.

### Response

Status: 204


## Create a group

### Payload
**name** `array` optional
Name of the group in one or more languages.

#### Example
~~~php
<?php

Array
(
    [0] => Array
        (
            [de-DE] => Entwicklung
            [en-GB] => Development
            [zh-Hans-HK] => 发展
        )

)
~~~

### Response

Status: 201
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 
| createdBy |  | 
| createdAt |  | 


## Delete a group

### Response

Status: 204


## Get a group

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 
| createdBy |  | 
| createdAt |  | 


## List all groups

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| 0 |  | 


## Remove a user from a group.

### Response

Status: 204


## Rename a group

### Payload
**name** `array` optional
Name of the group in one or more languages.

#### Example
~~~php
<?php

Array
(
    [0] => Array
        (
            [de-DE] => Entwicklung
            [en-GB] => Development
            [zh-Hans-HK] => 发展
        )

)
~~~

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 
| createdBy |  | 
| createdAt |  | 


## Assign a role to a group.

### Response

Status: 204


## Assign a role to a user.

### Response

Status: 204


## Create a role

### Payload
**name** `array` optional
Name of the role in one or more languages.

#### Example
~~~php
<?php

Array
(
    [0] => Array
        (
            [de-DE] => Entwicklung
            [en-GB] => Development
            [zh-Hans-HK] => 发展
        )

)
~~~
**type** `string` optional
Type of the role.
Valid values: Array
(
    [0] => USER
    [1] => ADMIN
    [2] => GUEST
    [3] => EXTERNAL
)


#### Example
~~~php
<?php

Array
(
    [0] => USER
)
~~~

### Response

Status: 201
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 
| type |  | 
| isPredefined |  | 


## Delete a role

### Response

Status: 204


## Get a role

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 
| type |  | 
| isPredefined |  | 


## List all roles

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| 0 |  | 


## Remove a role from a group.

### Response

Status: 204


## Remove a role from a user.

### Response

Status: 204


## Rename a role

### Payload
**name** `array` optional
Name of the role in one or more languages.

#### Example
~~~php
<?php

Array
(
    [0] => Array
        (
            [de-DE] => Entwicklung
            [en-GB] => Development
            [zh-Hans-HK] => 发展
        )

)
~~~

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 
| type |  | 
| isPredefined |  | 


## Create a user

### Payload
**organizationId** `string` optional
The Organization where the user is assigned to.

#### Example
~~~php
<?php

Array
(
    [0] => 680fe5ff-3b68-4d22-bb91-eb6a9712f78d
)
~~~
**username** `string` optional
The username of the user.

#### Example
~~~php
<?php

Array
(
    [0] => IronMan
)
~~~
**password** `string` optional
The password of the user.

#### Example
~~~php
<?php

Array
(
    [0] => 4-v3ry.53cr37_p455w0rd
)
~~~
**email** `string` optional
The email address of the user.

#### Example
~~~php
<?php

Array
(
    [0] => examples@examples.com
)
~~~
**name** `string` optional
The name of the user.

#### Example
~~~php
<?php

Array
(
    [0] => Robert Downey Jr.
)
~~~
**roles** `array` optional
The roles which should be assigned to the user.

#### Example
~~~php
<?php

Array
(
    [0] => Array
        (
            [0] => 680fe5ff-3b68-4d22-bb91-eb6a9712f78d
            [1] => 680fe5ff-3b68-4d22-bb91-eb6a9712f78d
        )

)
~~~

### Response

Status: 201
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| username |  | 
| email |  | 
| name |  | 
| status |  | 
| verified |  | 
| penultimateLoginAt |  | 
| createdAt |  | 


## Delete a preference for a user.

### Response

Status: 204


## Get a user

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| username |  | 
| email |  | 
| name |  | 
| status |  | 
| verified |  | 
| penultimateLoginAt |  | 
| createdAt |  | 


## Get a user identity

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| username |  | 
| email |  | 
| name |  | 
| status |  | 
| verified |  | 
| penultimateLoginAt |  | 
| createdAt |  | 


## List all users

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| 0 |  | 


## Get a user

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| username |  | 
| email |  | 
| name |  | 
| status |  | 
| verified |  | 
| penultimateLoginAt |  | 
| createdAt |  | 


## Get a user

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| username |  | 
| email |  | 
| name |  | 
| status |  | 
| verified |  | 
| penultimateLoginAt |  | 
| createdAt |  | 


## Get a user

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| username |  | 
| email |  | 
| name |  | 
| status |  | 
| verified |  | 
| penultimateLoginAt |  | 
| createdAt |  | 


## Set the password for a user.

### Payload
**password** `string` optional
The password of the user.

#### Example
~~~php
<?php

Array
(
    [0] => 4-v3ry.53cr37_p455w0rd
)
~~~
**securityToken** `string` optional
The security token to authenticate.

#### Example
~~~php
<?php

Array
(
)
~~~

### Response

Status: 204


## Set a preference for a user.

### Payload
**settingId** `string` optional
The ID of the configuration setting.

#### Example
~~~php
<?php

Array
(
    [0] => 680fe5ff-3b68-4d22-bb91-eb6a9712f78d
)
~~~
**value** `bool|int|string|array` optional
The value to set the configuration setting set to.

#### Example
~~~php
<?php

Array
(
    [0] => 1
    [1] => 1620979351
    [2] => Europe/Berlin
    [3] => Array
        (
            [de-DE] => Entwicklung
            [en-GB] => Development
            [zh-Hans-HK] => 发展
        )

)
~~~

### Response

Status: 204

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

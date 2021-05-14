# Organization REST API

This page provides a list of all organization REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Assign a user to an organization.

### Response

Status: 204


## Create a organization

### Payload
**name** `string` optional
Name of the organization.

#### Example
~~~php
<?php

Array
(
    [0] => ACME organization
)
~~~

### Response

Status: 201
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 


## Delete a organization

### Response

Status: 204


## Get a organization

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 


## List all organizations

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  | 


## Remove a user from an organization.

### Response

Status: 204


## Rename a organization

### Payload
**name** `string` optional
Name of the organization.

#### Example
~~~php
<?php

Array
(
    [0] => ACME organization
)
~~~

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| name |  |

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

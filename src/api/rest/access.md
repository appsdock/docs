# Access REST API

This page provides a list of all access REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Change a policy

### Payload
**effect** `string` optional
Effect of the policy.
Valid values: Array
(
    [0] => ALLOW
    [1] => DENY
)


#### Example
~~~php
<?php

Array
(
    [0] => ALLOW
)
~~~

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| actionId |  | 
| roleId |  | 
| resource |  | 
| effect |  | 


## Create a policy

### Payload
**roleId** `string` optional
Role ID for the policy.

#### Example
~~~php
<?php

Array
(
    [0] => 680fe5ff-3b68-4d22-bb91-eb6a9712f78d
)
~~~
**resource** `string` optional
Resource of the policy.
Valid values: Array
(
    [0] => *
    [1] => UUID
)


#### Example
~~~php
<?php

Array
(
    [0] => *
)
~~~
**effect** `string` optional
Effect of the policy.
Valid values: Array
(
    [0] => ALLOW
    [1] => DENY
)


#### Example
~~~php
<?php

Array
(
    [0] => ALLOW
)
~~~

### Response

Status: 201
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| actionId |  | 
| roleId |  | 
| resource |  | 
| effect |  | 


## Delete a policy

### Response

Status: 204


## List all policies

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| actionId |  | 
| roleId |  | 
| resource |  | 
| effect |  |

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

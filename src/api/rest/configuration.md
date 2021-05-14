# Configuration REST API

This page provides a list of all configuration REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Change a configuration setting

### Payload
**value** `bool|int|string|array` optional
Value of the configuration setting.

#### Example
~~~php
<?php

Array
(
    [0] => 
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


## Get a configuration setting

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| type |  | 
| value |  | 
| default |  | 
| options |  | 


## List all configuration settings

### Response

Status: 200
| Name | Type | Example
| ---- | :--: | -------
| id |  | 
| type |  | 
| value |  | 
| default |  | 
| options |  |

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

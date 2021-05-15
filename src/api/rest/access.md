# Access REST API

This page provides a list of all access REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## The policy resource

### Attributes

**id** `string`


**actionId** `string`


**roleId** `string`


**resource** `string`


**effect** `string`


### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "actionId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "roleId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "resource": "*",
    "effect": "ALLOW"
}
~~~

## Change a policy

### Parameters

**effect** `string` optional
Effect of the policy.

### Payload

~~~json
{
    "effect": "DENY"
}
~~~

## Create a policy

### Parameters

**roleId** `string` optional
Role ID for the policy.

**resource** `string` optional
Resource of the policy.

**effect** `string` optional
Effect of the policy.

### Payload

~~~json
{
    "roleId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "resource": [
        "*"
    ],
    "effect": "ALLOW"
}
~~~

## Delete a policy

### Parameters

This endpoint has no parameters.

## List all policies

### Parameters

This endpoint has no parameters.


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

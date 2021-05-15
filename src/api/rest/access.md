# Access REST API

This page provides a list of all access REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Change a policy

`POST` **/v1/policies/{id}**

### Parameters

| Parameter | Type | Required | Description
| --------- | :--: | :------: | -----------
| **effect** | `string` | ❌ | Effect of the policy.

### Payload

~~~json
{
    "effect": "DENY"
}
~~~

## Create a policy

`POST` **/v1/policies**

### Parameters

| Parameter | Type | Required | Description
| --------- | :--: | :------: | -----------
| **roleId** | `string` | ❌ | Role ID for the policy.
| **resource** | `string` | ❌ | Resource of the policy.
| **effect** | `string` | ❌ | Effect of the policy.

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

`DELETE` **/v1/policies/{id}**

### Parameters

!!! important "This endpoint has no parameters."

## List all policies

`GET` **/v1/policies**

### Parameters

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

*[✓]: Yes
*[❌]: No

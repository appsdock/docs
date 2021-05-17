# Access REST API

This page provides a list of all access REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Policy

### Resource

#### Attributes

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The policy ID in UUID format.
| **actionId** | `string` | The action ID in UUID format.
| **roleId** | `string` | The role ID in UUID format.
| **resource** | `string` | The resource affected by the policy.
| **effect** | `string` | The effect of the policy. The effect can be to either allow or prohibit access.

#### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "actionId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "roleId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "resource": "*",
    "effect": "ALLOW"
}
~~~

### Requests

#### Change a policy

`POST` **/v1/policies/{id}**

##### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **effect** | `string` | ✔ | The effect of the policy. The effect can be to either allow or prohibit access.

##### Payload

~~~json
{
    "effect": "DENY"
}
~~~

#### Create a policy

`POST` **/v1/policies**

##### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **roleId** | `string` | ✔ | The role ID in UUID format.
| **resource** | `string` | ✔ | The resource affected by the policy.
| **effect** | `string` | ✔ | The effect of the policy. The effect can be to either allow or prohibit access.

##### Payload

~~~json
{
    "roleId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "resource": "*",
    "effect": "ALLOW"
}
~~~

#### Delete a policy

`DELETE` **/v1/policies/{id}**

##### Parameters

!!! important "This endpoint has no parameters."

#### List all policies

`GET` **/v1/policies**

##### Parameters

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[ID]: Identifier
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

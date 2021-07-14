# Access Resources

This page provides a list of all access resource endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Action

### The Action resource
~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "appId": "28dfe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "action": "document.read",
    "name": "Read documents",
    "description": "Permits the read action for documents."
}
~~~

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The action ID in UUID format.
| **appId** | `string` | The app ID in UUID format.
| **action** | `string` | The action short id.
| **name** | `string` | The name of the action.
| **description** | `string` | The description of the action.


### List all actions

`GET` **/v1/actions**


**Parameters**

!!! important "This endpoint has no parameters."
## Policy

### The Policy resource
~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "actionId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "roleId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "resource": "*",
    "effect": "ALLOW"
}
~~~

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The policy ID in UUID format.
| **actionId** | `string` | The action ID in UUID format.
| **roleId** | `string` | The role ID in UUID format.
| **resource** | `string` | The resource affected by the policy. Valid values are: *, `UUID`
| **effect** | `string` | The effect of the policy. The effect can be to either allow or prohibit access. Valid values are: ALLOW, DENY


### Change a policy

`POST` **/v1/policies/{id}**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **effect** | `string` | ✔ | The effect of the policy. The effect can be to either allow or prohibit access. Valid values are: ALLOW, DENY

##### Payload

~~~json
{
    "effect": "DENY"
}
~~~

### Create a policy

`POST` **/v1/policies**


**Parameters**

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **roleId** | `string` | ✔ | The role ID in UUID format.
| **resource** | `string` | ✔ | The resource affected by the policy. Valid values are: *, `UUID`
| **actionId** | `string` | ✔ | The action ID in UUID format.
| **effect** | `string` | ✔ | The effect of the policy. The effect can be to either allow or prohibit access. Valid values are: ALLOW, DENY

##### Payload

~~~json
{
    "roleId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "resource": "*",
    "actionId": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "effect": "ALLOW"
}
~~~

### Delete a policy

`DELETE` **/v1/policies/{id}**


**Parameters**

!!! important "This endpoint has no parameters."

### List all policies

`GET` **/v1/policies**


**Parameters**

!!! important "This endpoint has no parameters."


*[API]: Application Programming Interface
*[ID]: Identifier
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

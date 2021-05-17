# Organization REST API

This page provides a list of all organization REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Organization

### Resource

#### Attributes

| Attribute | Type | Description
| --------- | ---- | -----------
| **id** | `string` | The identifier of the organization as UUID.
| **name** | `string` | The name of the organization.

#### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": "Stark Industries"
}
~~~

### Requests

#### Assign a user to an organization

`POST` **/v1/organizations/{organizationId}/users/{userId}**

##### Parameters

!!! important "This endpoint has no parameters."

#### Create a organization

`POST` **/v1/organizations**

##### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `string` | ✔ | The name of the organization.

##### Payload

~~~json
{
    "name": "Stark Industries"
}
~~~

#### Delete a organization

`DELETE` **/v1/organizations/{id}**

##### Parameters

!!! important "This endpoint has no parameters."

#### Get a organization

`GET` **/v1/organizations/{id}**

!!! info "Description"
    Returns an object of the organization. If the organization is inactive an 404 Not Found error will be returned instead.

##### Parameters

!!! important "This endpoint has no parameters."

#### List all organizations

`GET` **/v1/organizations**

!!! info "Description"
    Returns a object collection of all organizations. Inactive organizations are excluded.

##### Parameters

!!! important "This endpoint has no parameters."

#### Remove a user from an organization

`DELETE` **/v1/organizations/{organizationId}/users/{userId}**

##### Parameters

!!! important "This endpoint has no parameters."

#### Rename a organization

`POST` **/v1/organizations/{id}**

##### Parameters

| Parameter | Type | Required | Description
| --------- | ---- | :------: | -----------
| **name** | `string` | ✔ | The name of the organization.

##### Payload

~~~json
{
    "name": "Stark Industries"
}
~~~


*[API]: Application Programming Interface
*[ID]: Identifier
*[OS]: Operating System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

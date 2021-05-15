# Organization REST API

This page provides a list of all organization REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## The organization resource

### Attributes

**id** `string`
The identifier of the organization as UUID.

**name** `string`
The name of the organization.

### Response

~~~json
{
    "id": "680fe5ff-3b68-4d22-bb91-eb6a9712f78d",
    "name": "Stark Industries"
}
~~~

## Assign a user to an organization.

### Parameters

This endpoint has no parameters.

## Create a organization

### Parameters

**name** `string` optional
The name of the organization.

### Payload

~~~json
{
    "name": "Stark Industries"
}
~~~

## Delete a organization

### Parameters

This endpoint has no parameters.

## Get a organization

!!! info "Description"
    Returns an object of the organization. If the organization is inactive an 404 Not Found error will be returned instead.

### Parameters

This endpoint has no parameters.

## List all organizations

!!! info "Description"
    Returns a object collection of all organizations. Inactive organizations are excluded.

### Parameters

This endpoint has no parameters.

## Remove a user from an organization.

### Parameters

This endpoint has no parameters.

## Rename a organization

### Parameters

**name** `string` optional
The name of the organization.

### Payload

~~~json
{
    "name": "Stark Industries"
}
~~~


*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

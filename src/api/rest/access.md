# Access REST API

This page provides a list of all access REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Create Policy

| Route | Method | Version
| ----- | ------ | ------:
| `/policies` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Access &#10095; API &#10095; PolicyWriteRestAPI`            
    Method: `createPolicy`

## Change Policy

| Route | Method | Version
| ----- | ------ | ------:
| `/policies/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Access &#10095; API &#10095; PolicyWriteRestAPI`            
    Method: `changePolicy`

## Delete Policy

| Route | Method | Version
| ----- | ------ | ------:
| `/policies/{id}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Access &#10095; API &#10095; PolicyWriteRestAPI`            
    Method: `deletePolicy`

## List Policies

| Route | Method | Version
| ----- | ------ | ------:
| `/policies` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Access &#10095; API &#10095; PolicyReadRestAPI`            
    Method: `listPolicies`

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

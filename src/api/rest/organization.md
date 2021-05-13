# Organization REST API

This page provides a list of all organization REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## List Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/organizations` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Organization &#10095; API &#10095; OrganizationReadRestAPI`            
    Method: `listOrganization`

## Get Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/organizations/{id}` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Organization &#10095; API &#10095; OrganizationReadRestAPI`            
    Method: `getOrganization`

## Create Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/organizations` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Organization &#10095; API &#10095; OrganizationWriteRestAPI`            
    Method: `createOrganization`

## Rename Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/organizations/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Organization &#10095; API &#10095; OrganizationWriteRestAPI`            
    Method: `renameOrganization`

## Delete Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/organizations/{id}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Organization &#10095; API &#10095; OrganizationWriteRestAPI`            
    Method: `deleteOrganization`

## Assign User To Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/organizations/{organizationId}/users/{userId}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Organization &#10095; API &#10095; OrganizationWriteRestAPI`            
    Method: `assignUserToOrganization`

## Remove User From Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/organizations/{organizationId}/users/{userId}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Organization &#10095; API &#10095; OrganizationWriteRestAPI`            
    Method: `removeUserFromOrganization`

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

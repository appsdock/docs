# Organization REST API

This page provides a list of all organization REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## List Organization

| Route | Method | Version
| ----- | ------ | ------:
| /organizations | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Organization ❯ API ❯ OrganizationReadRestAPI ❯ listOrganization

## Get Organization

| Route | Method | Version
| ----- | ------ | ------:
| /organizations/{id} | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Organization ❯ API ❯ OrganizationReadRestAPI ❯ getOrganization

## Create Organization

| Route | Method | Version
| ----- | ------ | ------:
| /organizations | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Organization ❯ API ❯ OrganizationWriteRestAPI ❯ createOrganization

## Rename Organization

| Route | Method | Version
| ----- | ------ | ------:
| /organizations/{id} | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Organization ❯ API ❯ OrganizationWriteRestAPI ❯ renameOrganization

## Delete Organization

| Route | Method | Version
| ----- | ------ | ------:
| /organizations/{id} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Organization ❯ API ❯ OrganizationWriteRestAPI ❯ deleteOrganization

## Assign User To Organization

| Route | Method | Version
| ----- | ------ | ------:
| /organizations/{organizationId}/users/{userId} | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Organization ❯ API ❯ OrganizationWriteRestAPI ❯ assignUserToOrganization

## Remove User From Organization

| Route | Method | Version
| ----- | ------ | ------:
| /organizations/{organizationId}/users/{userId} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Organization ❯ API ❯ OrganizationWriteRestAPI ❯ removeUserFromOrganization

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

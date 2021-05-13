# Identity REST API

This page provides a list of all identity REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## List Roles

| Route | Method | Version
| ----- | ------ | ------:
| `/roles` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleReadRestAPI`            
    Method: `listRoles`

## Get Role

| Route | Method | Version
| ----- | ------ | ------:
| `/roles/{id}` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleReadRestAPI`            
    Method: `getRole`

## List Group

| Route | Method | Version
| ----- | ------ | ------:
| `/groups` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; GroupReadRestAPI`            
    Method: `listGroup`

## Get Group

| Route | Method | Version
| ----- | ------ | ------:
| `/groups/{id}` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; GroupReadRestAPI`            
    Method: `getGroup`

## Create Group

| Route | Method | Version
| ----- | ------ | ------:
| `/groups` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; GroupWriteRestAPI`            
    Method: `createGroup`

## Rename Group

| Route | Method | Version
| ----- | ------ | ------:
| `/groups/{id}` | `PATCH` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; GroupWriteRestAPI`            
    Method: `renameGroup`

## Delete Group

| Route | Method | Version
| ----- | ------ | ------:
| `/groups/{id}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; GroupWriteRestAPI`            
    Method: `deleteGroup`

## Assign User To Group

| Route | Method | Version
| ----- | ------ | ------:
| `/groups/{groupId}/users/{userId}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; GroupWriteRestAPI`            
    Method: `assignUserToGroup`

## Remove User From Group

| Route | Method | Version
| ----- | ------ | ------:
| `/groups/{groupId}/users/{userId}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; GroupWriteRestAPI`            
    Method: `removeUserFromGroup`

## Create Users

| Route | Method | Version
| ----- | ------ | ------:
| `/users` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserWriteRestAPI`            
    Method: `createUsers`

## Set Password

| Route | Method | Version
| ----- | ------ | ------:
| `/users/{id}/password` | `PATCH` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserWriteRestAPI`            
    Method: `setPassword`

## Set User Preference

| Route | Method | Version
| ----- | ------ | ------:
| `/users/me/preferences` | `PUT` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserWriteRestAPI`            
    Method: `setUserPreference`

## Remove User From Organization

| Route | Method | Version
| ----- | ------ | ------:
| `/users/me/preferences/{settingId}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserWriteRestAPI`            
    Method: `removeUserFromOrganization`

## List Users

| Route | Method | Version
| ----- | ------ | ------:
| `/users` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserReadRestAPI`            
    Method: `listUsers`

## Get

| Route | Method | Version
| ----- | ------ | ------:
| `/users/{id}` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserReadRestAPI`            
    Method: `get`

## Get Secured Identity

| Route | Method | Version
| ----- | ------ | ------:
| `/users/{id}/identity/{securityToken}` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserReadRestAPI`            
    Method: `getSecuredIdentity`

## Get Me

| Route | Method | Version
| ----- | ------ | ------:
| `/users/me` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserReadRestAPI`            
    Method: `getMe`

## List Me Policies

| Route | Method | Version
| ----- | ------ | ------:
| `/users/me/policies` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserReadRestAPI`            
    Method: `listMePolicies`

## List Me Preferences

| Route | Method | Version
| ----- | ------ | ------:
| `/users/me/preferences` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; UserReadRestAPI`            
    Method: `listMePreferences`

## Create Role

| Route | Method | Version
| ----- | ------ | ------:
| `/roles` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleWriteRestAPI`            
    Method: `createRole`

## Rename Role

| Route | Method | Version
| ----- | ------ | ------:
| `/roles/{id}` | `PATCH` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleWriteRestAPI`            
    Method: `renameRole`

## Delete Role

| Route | Method | Version
| ----- | ------ | ------:
| `/roles/{id}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleWriteRestAPI`            
    Method: `deleteRole`

## Assign Role To User

| Route | Method | Version
| ----- | ------ | ------:
| `/roles/{roleId}/users/{userId}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleWriteRestAPI`            
    Method: `assignRoleToUser`

## Assign Role To Group

| Route | Method | Version
| ----- | ------ | ------:
| `/roles/{roleId}/groups/{groupId}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleWriteRestAPI`            
    Method: `assignRoleToGroup`

## Remove Role From User

| Route | Method | Version
| ----- | ------ | ------:
| `/roles/{roleId}/users/{userId}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleWriteRestAPI`            
    Method: `removeRoleFromUser`

## Remove Role From Group

| Route | Method | Version
| ----- | ------ | ------:
| `/roles/{roleId}/groups/{groupId}` | `DELETE` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Identity &#10095; API &#10095; RoleWriteRestAPI`            
    Method: `removeRoleFromGroup`

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

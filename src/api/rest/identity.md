# Identity REST API

This page provides a list of all identity REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## List Roles

| Route | Method | Version
| ----- | ------ | ------:
| /roles | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleReadRestAPI ❯ listRoles

## Get Role

| Route | Method | Version
| ----- | ------ | ------:
| /roles/{id} | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleReadRestAPI ❯ getRole

## List Group

| Route | Method | Version
| ----- | ------ | ------:
| /groups | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ GroupReadRestAPI ❯ listGroup

## Get Group

| Route | Method | Version
| ----- | ------ | ------:
| /groups/{id} | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ GroupReadRestAPI ❯ getGroup

## Create Group

| Route | Method | Version
| ----- | ------ | ------:
| /groups | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ GroupWriteRestAPI ❯ createGroup

## Rename Group

| Route | Method | Version
| ----- | ------ | ------:
| /groups/{id} | `PATCH` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ GroupWriteRestAPI ❯ renameGroup

## Delete Group

| Route | Method | Version
| ----- | ------ | ------:
| /groups/{id} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ GroupWriteRestAPI ❯ deleteGroup

## Assign User To Group

| Route | Method | Version
| ----- | ------ | ------:
| /groups/{groupId}/users/{userId} | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ GroupWriteRestAPI ❯ assignUserToGroup

## Remove User From Group

| Route | Method | Version
| ----- | ------ | ------:
| /groups/{groupId}/users/{userId} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ GroupWriteRestAPI ❯ removeUserFromGroup

## Create Users

| Route | Method | Version
| ----- | ------ | ------:
| /users | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserWriteRestAPI ❯ createUsers

## Set Password

| Route | Method | Version
| ----- | ------ | ------:
| /users/{id}/password | `PATCH` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserWriteRestAPI ❯ setPassword

## Set User Preference

| Route | Method | Version
| ----- | ------ | ------:
| /users/me/preferences | `PUT` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserWriteRestAPI ❯ setUserPreference

## Remove User From Organization

| Route | Method | Version
| ----- | ------ | ------:
| /users/me/preferences/{settingId} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserWriteRestAPI ❯ removeUserFromOrganization

## List Users

| Route | Method | Version
| ----- | ------ | ------:
| /users | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserReadRestAPI ❯ listUsers

## Get

| Route | Method | Version
| ----- | ------ | ------:
| /users/{id} | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserReadRestAPI ❯ get

## Get Secured Identity

| Route | Method | Version
| ----- | ------ | ------:
| /users/{id}/identity/{securityToken} | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserReadRestAPI ❯ getSecuredIdentity

## Get Me

| Route | Method | Version
| ----- | ------ | ------:
| /users/me | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserReadRestAPI ❯ getMe

## List Me Policies

| Route | Method | Version
| ----- | ------ | ------:
| /users/me/policies | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserReadRestAPI ❯ listMePolicies

## List Me Preferences

| Route | Method | Version
| ----- | ------ | ------:
| /users/me/preferences | `GET` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ UserReadRestAPI ❯ listMePreferences

## Create Role

| Route | Method | Version
| ----- | ------ | ------:
| /roles | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleWriteRestAPI ❯ createRole

## Rename Role

| Route | Method | Version
| ----- | ------ | ------:
| /roles/{id} | `PATCH` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleWriteRestAPI ❯ renameRole

## Delete Role

| Route | Method | Version
| ----- | ------ | ------:
| /roles/{id} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleWriteRestAPI ❯ deleteRole

## Assign Role To User

| Route | Method | Version
| ----- | ------ | ------:
| /roles/{roleId}/users/{userId} | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleWriteRestAPI ❯ assignRoleToUser

## Assign Role To Group

| Route | Method | Version
| ----- | ------ | ------:
| /roles/{roleId}/groups/{groupId} | `POST` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleWriteRestAPI ❯ assignRoleToGroup

## Remove Role From User

| Route | Method | Version
| ----- | ------ | ------:
| /roles/{roleId}/users/{userId} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleWriteRestAPI ❯ removeRoleFromUser

## Remove Role From Group

| Route | Method | Version
| ----- | ------ | ------:
| /roles/{roleId}/groups/{groupId} | `DELETE` | 1

!!! important "Developer"
    AppsDock ❯ System ❯ Application ❯ Identity ❯ API ❯ RoleWriteRestAPI ❯ removeRoleFromGroup

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

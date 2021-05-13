# App REST API

This page provides a list of all app REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## List Apps

| Route | Method | Version
| ----- | ------ | ------:
| `/apps` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; App &#10095; API &#10095; AppReadRestAPI`            
    Method: `listApps`

## Install

| Route | Method | Version
| ----- | ------ | ------:
| `/apps:install/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; App &#10095; API &#10095; AppWriteRestAPI`            
    Method: `install`

## Uninstall

| Route | Method | Version
| ----- | ------ | ------:
| `/apps:uninstall/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; App &#10095; API &#10095; AppWriteRestAPI`            
    Method: `uninstall`

## Update

| Route | Method | Version
| ----- | ------ | ------:
| `/apps:update/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; App &#10095; API &#10095; AppWriteRestAPI`            
    Method: `update`

## Activate

| Route | Method | Version
| ----- | ------ | ------:
| `/apps:activate/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; App &#10095; API &#10095; AppWriteRestAPI`            
    Method: `activate`

## Deactivate

| Route | Method | Version
| ----- | ------ | ------:
| `/apps:deactivate/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; App &#10095; API &#10095; AppWriteRestAPI`            
    Method: `deactivate`

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

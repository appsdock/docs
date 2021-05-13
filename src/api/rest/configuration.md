# Configuration REST API

This page provides a list of all configuration REST API endpoints within AppsDock OS.

The guideline for the REST API can be found [here](../../../gettingstarted/guidelines/rest-api).

## Change Setting

| Route | Method | Version
| ----- | ------ | ------:
| `/settings/{id}` | `POST` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Configuration &#10095; API &#10095; SettingWriteRestAPI`            
    Method: `changeSetting`

## List Setting

| Route | Method | Version
| ----- | ------ | ------:
| `/settings` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Configuration &#10095; API &#10095; SettingReadRestAPI`            
    Method: `listSetting`

## Get Setting

| Route | Method | Version
| ----- | ------ | ------:
| `/settings/{id}` | `GET` | **1**

!!! important "Developer"
    Class: `AppsDock &#10095; System &#10095; Application &#10095; Configuration &#10095; API &#10095; SettingReadRestAPI`            
    Method: `getSetting`

*[API]: Application Programming Interface
*[OS]: Operating System
*[REST]: Representational State Transfer

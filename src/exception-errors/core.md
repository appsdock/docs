
# Core exception errors

This page provides a list of all core exception errors within AppsDock OS.

The guideline for exception errors can be found [here](../../gettingstarted/guidelines/exception-errors).

## General

### 10001

!!! danger "The setting has the wrong type."
    When validating the data type of the value of the setting, it was found that it does not correspond to the expected data type.
#### Reasons

- The data type of the value of the setting is not of the expected data type.
- The data type of the value of the setting was of the expected data type, but changed during transportation.

#### Solutions

- Change the data type of the value of the setting to the expected data type.
- Check your network for `HTTP` `POST` manipulation by firewalls or proxies.

### 10005

!!! danger "The option is not in the list of allowed options."
    When validating the value of the setting, it was found that it does not correspond to the allowed values.

### 10006

!!! danger "Some options are not in the list of allowed options."
    When validating the values of the setting, it was found that some do not correspond to the allowed values.

### 10007

!!! danger "The setting is not a valid date."
    When validating the value of the setting, it was found that it does not correspond to a date. A valid date format is `0000-00-00`.

### 10008

!!! danger "The setting is not a valid time."
    When validating the value of the setting, it was found that it does not correspond to a time. A valid time format is `00:00:00`.

### 10009

!!! danger "The setting does not exist."
    When reading the setting in the configuration, it was found that the setting does not exist.

### 10010

!!! danger "The setting does not exist."
    When changing the setting in the configuration, it was found that the setting does not exist.

### 10011

!!! danger "The setting does not exist."
    When resetting the setting in the configuration, it was found that the setting does not exist.

### 10012

!!! danger "The setting does not exist."
    When setting the setting in the user preferences, it was found that the setting does not exist.

### 10013

!!! danger "System cannot be uninstalled via app lifecycle management."
    

### 10014

!!! danger "Invalid/malformed database setup definition files."
    

### 10015

!!! danger "An error occurred while setup schema via database descriptor for database lifecycle operations."
    


## Infrastructure

PH_INFRASTRUCTURE

## Security & Authentication

PH_SECURITY_AUTHENTICATION

## Internal communication

PH_INTERNAL_COMMUNICATION

*[HTTP]: Hypertext Transfer Protocol
*[OS]: Operating System
*[SSH]: Secure Shell


# Exceptions

This list provides an overview of all exception errors within AppsDock OS.
For every error the list provides a more detailed description with possible causes and solutions.

## 10001

!!! danger "The setting has the wrong type."
    When validating the data type of the value of the setting, it was found that it does not correspond to the expected data type `BOOLEAN`.
### Reasons

- The data type of the value of the setting is not of the data type `BOOLEAN`.
- The data type of the value of the setting was `BOOLEAN`, but changed during transportation.
### Solutions

- Change the data type of the value of the setting to `BOOLEAN`.
- Check your network for `HTTP` `POST` manipulation by firewalls or proxies.


## 10002

!!! danger "The setting has the wrong type."
    When validating the data type of the value of the setting, it was found that it does not correspond to the expected data type `STRING`.


## 10003

!!! danger "The setting has the wrong type."
    When validating the data type of the value of the setting, it was found that it does not correspond to the expected data type `INTEGER`.


## 10004

!!! danger "The setting has the wrong type."
    When validating the data type of the value of the setting, it was found that it does not correspond to the expected data type `ARRAY`.


## 10005

!!! danger "The option is not in the list of allowed options."
    When validating the value of the setting, it was found that it does not correspond to the allowed values.


## 10006

!!! danger "Some options are not in the list of allowed options."
    When validating the values of the setting, it was found that some do not correspond to the allowed values.


## 10007

!!! danger "The setting is not a valid date."
    When validating the value of the setting, it was found that it does not correspond to a date. A valid date format is `0000-00-00`.


## 10008

!!! danger "The setting is not a valid time."
    When validating the value of the setting, it was found that it does not correspond to a time. A valid time format is `00:00:00`.


## 10009

!!! danger "The setting does not exist."
    When reading the setting in the configuration, it was found that the setting does not exist.


## 10010

!!! danger "The setting does not exist."
    When changing the setting in the configuration, it was found that the setting does not exist.


## 10011

!!! danger "The setting does not exist."
    When resetting the setting in the configuration, it was found that the setting does not exist.


## 10012

!!! danger "The setting does not exist."
    When setting the setting in the user preferences, it was found that the setting does not exist.


## 12000

!!! danger "The SSH key pairs for this installation could not be found."
    Unfortunately, there is currently no detailed description available.
### Reasons

- AppsDock OS is not installed yet.
- Could not create SSH key pairs.
### Solutions

- Check current installation and eventually run `adk install`
- Run `adk util:ssh-gen` for generating new key pairs. Please note: All current auth session will not work anymore.


## 12001

!!! danger "The username does not match with any existing user."
    Unfortunately, there is currently no detailed description available.
### Reasons

- The entered username does not exist.
- The password entered is incorrect or does not belong to the user name.
### Solutions

- Check the username and try again.
- Account may not exist now, please contact your account administrator.


## 12002

!!! danger "The initialized user account not enabled for authentication."
    Unfortunately, there is currently no detailed description available.
### Reason

- The user account has been created recently and requires an action of the account owner for activation.
### Solutions

- Check your email inbox for an activation email and complete the account activation by following the instructions.
- Contact the user account administrator and request for a new activation email.


## 12003

!!! danger "A potential bruteforce attack was detected."
    Unfortunately, there is currently no detailed description available.
### Reason

- Frequently failed login attempts.
### Solution

- Try again shortly.


## 12004

!!! danger "The password is wrong."
    Unfortunately, there is currently no detailed description available.
### Reason

- Username or password is wrong.
### Solution

- Check entered username and password and try again.


## 12005

!!! danger "The user account is locked."
    Unfortunately, there is currently no detailed description available.
### Solution

- Contact the user account administrator.


## 12006

!!! danger "The user account is inactive."
    Unfortunately, there is currently no detailed description available.
### Solution

- Contact the user account administrator.


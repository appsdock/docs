
# Exception errors

This page provides a list of all exception errors within AppsDock OS.
The guideline for exception errors can be found under **Getting Started &#10095; Guidelines &#10095; [Exception errors](../gettingstarted/guidelines/exceptions)**.

## 10001

!!! danger "The setting has the wrong type."
    When validating the data type of the value of the setting, it was found that it does not correspond to the expected data type.
### Reasons

- The data type of the value of the setting is not of the expected data type.
- The data type of the value of the setting was of the expected data type, but changed during transportation.

### Solutions

- Change the data type of the value of the setting to the expected data type.
- Check your network for `HTTP` `POST` manipulation by firewalls or proxies.

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

## 10013

!!! danger "System cannot be uninstalled via app lifecycle management."
    

## 10014

!!! danger "Invalid/malformed database setup definition files."
    

## 10015

!!! danger "An error occurred while setup schema via database descriptor for database lifecycle operations."
    

## 11000

!!! danger "An error occurred while connecting to the database."
    

## 11001

!!! danger "An error occurred while setup the ORM."
    

## 11002

!!! danger "An error occurred during executing a sql statement."
    

## 11003

!!! danger "An error occurred during ORM operations."
    

## 11004

!!! danger "An error occurred while execute statement for creating a new database."
    

## 11005

!!! danger "An error occurred while execute statement for database table creation."
    

## 11006

!!! danger "An error occurred while execute statement for delete database."
    

## 11007

!!! danger "An error occurred while execute statement during database migration."
    

## 11008

!!! danger "An error occurred while operate with database via ORM."
    

## 11009

!!! danger "An error occurred while database operation via cli."
    

## 11010

!!! danger "An error occurred while execute statement to copy database/schema."
    

## 12000

!!! danger "The server is currently not available."
    
### Reasons

- AppsDock OS is not installed yet.
- Could not create SSH key pairs.

### Solutions

- Check current installation and eventually run `adk install`
- Run `adk util:ssh-gen` for generating new key pairs. Please note, that all current auth sessions will not work anymore.

## 12001

!!! danger "The username or password is wrong."
    
### Reasons

- The entered username does not exist.
- The password entered is incorrect or does not belong to the user name.

### Solutions

- Check the username and try again.
- Account may not exist now, please contact your account administrator.

## 12002

!!! danger "The account is not available yet."
    
### Reason

- The user account has been created recently and requires an action of the account owner for activation.

### Solutions

- Check your email inbox for an activation email and complete the account activation by following the instructions.
- Contact the user account administrator and request for a new activation email.

## 12003

!!! danger "Your account is temporary suspended because of too many failed logins."
    
### Reason

- Frequently failed login attempts.

### Solution

- Try again shortly.

## 12004

!!! danger "The credentials were incorrect."
    
### Reason

- Username or password is wrong.

### Solution

- Check entered username and password and try again.

## 12005

!!! danger "The user account is locked."
    
### Solution

- Contact the user account administrator.

## 12006

!!! danger "The user account is inactive."
    
### Solution

- Contact the user account administrator.

## 12007

!!! danger "Access denied due to insufficient permissions."
    
### Reasons

- The users role does not have the policy that permits the required action.
- The user is not assigned to the role which is already permitted.

### Solutions

- Assign the policy that permits the required action to the users role.
- Assign the user to the role which is already permitted.

## 12008

!!! danger "Access denied due to insufficient authority."
    
### Reason

- The user is not authorized/signed in.

### Solution

- The user has to sign in with personal credentials.


*[HTTP]: Hypertext Transfer Protocol
*[OS]: Operating System
*[SSH]: Secure Shell

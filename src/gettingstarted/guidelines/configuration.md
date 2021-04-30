# Configuration

## Setting ID

The first part of the ID of a setting is always composed of the app context, such as **com.appsdock** or **com.appsdock.hrm**, followed by the identifier **config**. This is followed by a colon as a separator. The second part consists of any (or none) grouping separated by dots. The last word is the name of the setting.

### Examples

| Context | Identifier[^1] | Separator | Group[^2] | Name
| ------- | :------------: | :-------: | --------- | ----
| com.appsdock | .config | : | maintenance | date
| com.appsdock | .config | : | email.smtp | username
| com.appsdock.hrm | .config | : | leave | max

## Setting types

| ID | Name | Description
| -- | ---- | -----------
| `BOOL` | True \| False | A "either or" choice.
| `STRING` | String | A string. It's the **default**.
| `INT` | Number | A signed number.
| `SELECT` | Selection | A single selection of options.
| `MULTISELECT` | Multi selection | A multiple selection of options.
| `DATE` | Date | A date.
| `TIME` | Time | A time.

## Default value

The default value is used if no value has been set by the user. Therefore, it can be easily overwritten during updates. If a value has been set by the user, it remains unaffected.

The possibility to change the values is managed via the rights system. There are settings that cannot be changed by normal administrators, so the default value is always used here.

## Database

| Field | Type
| ----- | ----
| id | `VARCHAR(255)`
| type | `ENUM('BOOL', 'STRING', 'INT', 'SELECT', 'MULTISELECT', 'DATE', 'TIME')`
| value | `JSON`
| default | `JSON`
| options | `JSON`

### Examples

| id | type | value | default | options
| -- | ---- | ----- | ------- | -------
| com.appsdock.config:email.smtp.authentication | `BOOL` | `[true]` | `[]` | `[]`
| com.appsdock.config:email.smtp.username | `STRING` | `["example@example.com"]` | `[]` | `[]`
| com.appsdock.config:email.smtp.connection.retries | `INT` | `[10]` | `[5]` | `[]`
| com.appsdock.hrm.config:notification.email.interval | `SELECT` | `["daily"]` | `["weekly"]` | `["daily", "weekly", "monthly"]`
| com.appsdock.config:notification.channels | `MULTISELECT` | `["browser", "email", "discord"]` | `["browser"]` | `["browser", "email", "discord", "telegram", "whatsapp", "sms"]}`
| com.appsdock.config:maintenance.date | `DATE` | `["2021-06-01"]}` | `[]`
| com.appsdock.config:maintenance.time | `TIME` | `["14:35"]` | `[]`

[^1]: The identifier for configuration settings is always **config**.
[^2]: A group is **optional**.

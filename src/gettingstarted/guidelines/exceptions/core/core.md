# Core

## Error codes

| Code | Description
| ---: | -----------
| [10001](#10001) | When validating the data type of the value of the setting, it was found that it does not correspond to the allowed type `BOOLEAN`.
| [10002](#10002) | When validating the data type of the value of the setting, it was found that it does not correspond to the allowed type `STRING`.
| [10003](#10003) | When validating the data type of the value of the setting, it was found that it does not correspond to the allowed type `INTEGER`.
| [10004](#10004) | When validating the data type of the value of the setting, it was found that it does not correspond to the allowed type `ARRAY`.
| [10005](#10005) | When validating the format of the value of the setting, it was found that it is not a permitted value.
| [10006](#10006) | When validating the format of the value of the setting, it was found that it is not one or more of the permitted values.
| [10007](#10007) | When validating the format of the value of the setting, it was found that it is not a valid date format.
| [10008](#10008) | When validating the format of the value of the setting, it was found that it is not a valid time format.
| [10009](#10009) | When trying to read out the setting from the configuration, it was found that it does not exist.

## 10001

* The data type of the value of the setting was passed incorrectly.

## 10002

* The data type of the value of the setting was passed incorrectly.

## 10003

* The data type of the value of the setting was passed incorrectly.

## 10004

* The data type of the value of the setting was passed incorrectly.

## 10005

## 10006

## 10007

## 10008

## 10009

* The ID of the setting is wrong.
* The context of the setting is wrong because it is missing or has been passed incorrectly[^1].

[^1]: If no valid context is passed, AppsDock OS uses the default context.

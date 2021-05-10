# Exception errors

AppsDock OS has the following three main exception errors classes.

* **Exception**
* **LogicException**
* **RuntimeException**

All three implement the **ExceptionInterface** and use the **ExceptionTrait** to provide useful information for finding the cause and fixing the problem. They are all located at **AppsDock &#10095; Core &#10095; Common &#10095; Exception**.

!!! warning "Convention"
    Every AppsDock OS exception **must** inherit from one of these exception classes.

## Usage

Each exception error has three parameters.
The first parameter is the error code which must adhere to the [conventions](#conventions).
The second parameter may contain additional information.
The third parameter may contain a preceding exception error.

~~~php
<?php

/**
 * ExampleException
 *
 * @param array $ex
 * @param array $details
 * @param Throwable|null $previous
 */
public function __construct(array $ex, array $details = [], Throwable $previous = null)
{
    ...
}

throw new ExampleException(EX_00000, ['Variable 1' => $var1, 'Variable 2' => $var2], $previous);
~~~

### Error codes

An error code is created as a `ARRAY` constant under **AppsDock OS &#10095; application &#10095; config &#10095; exceptions.php**.
The constant name must start with `EX_` followed by a 5-digit **unique** number.

An error code constant must always contain the error code itself and a message.

Optionally, a public message can be included, which is then shown to users instead of the actual message.
The description is also not mandatory if the message is already meaningful enough.

Optionally, reasons and solutions for the exception error can be given.

~~~php
<?php

const EX_00000 = [
    'code' => 00000,
    'message' => 'The variable has the wrong data type.',
    'publicMessage' => 'Something is wrong. Please try again later.'
    'description' => 'When validating the data type ...',
    'reasons' => [
        'The data type is not the expected data type.',
        '...'
    ],
    'solutions' => [
        'Change the data type of the variable.',
        '...'
    ]
];
~~~

## Conventions

### Error code ranges

| Range | Context | Scope | Description
| ----: | ------- | ----- | -----------
| 10.000 | Core | | AppsDock OS core components.
| 11.000 | | Infrastructure | AppsDock OS core infrastructure components.
| 12.000 | | Security & authentication | AppsDock OS core security and authentication components.
| 13.000 | | Internal communication | AppsDock OS core internal communication components.
| 20.000 | System | | AppsDock OS system components.
| 30.000 | Integration | | Third party API services, like an email service provider.
| 40.000 | Plugin | | Small application to extend AppsDock OS or app functionality.
| 90.000[^1] | Apps | | Applications build with AppsDock OS.

[^1]: The ranges from 50.000 to 80.000 are reserved for future use.

*[API]: Application Programming Interface
*[PHP]: PHP: Hypertext Preprocessor
*[OS]: Operating System

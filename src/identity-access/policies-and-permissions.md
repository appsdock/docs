# Policies and permissions

## Permission

A permission consists of one or more policies.

### Examples

The permission **DMS user** has the indefinite right to read within the entire DMS and the definite right to write in its own folders.

| Policy | Action | Role | Resource | Effect
| ------ | ------ | :--: | :------: | :----:
| `READ` | com.appsdock.dms.action:read | UUID | **\*** | `ALLOW`
| `WRITE` | com.appsdock.dms.action:write | UUID | `ALLOW`

## Policy

A policy consists of the action, role, resource and effect.

### Action

Actions are defined by the apps.

#### Example

The DMS app defines the action **Create folder**.

### Role

Exactly one role must be assigned per policy.

### Resource

A resource can be defined or undefined. Indefinite resources are defined by means of the **\***.

### Effect

The effect is either **allow** or **deny**.

## Permission control

The permission control is given the action as the first parameter, and the context as the second parameter.

~~~php
<?php

$isPermitted = $this->permissionController->isPermitted(
'read',
$this->context->getId()
);
~~~

Given a specific resource, its UUID is given as the third parameter.

~~~php
<?php

$isPermitted = $this->permissionController->isPermitted(
    'read',
    $this->context->getId(),
    $appId
);
~~~

Alternatively, a default value can be specified as the fourth parameter. This is only returned if **no** policy exists.

~~~php
<?php

$isPermitted = $this->permissionController->isPermitted(
    'read',
    $this->context->getId(),
    $appId,
    $default
);
~~~

## REST API

Permissions are defined as [method-attribute](#method-attribute) or alternatively as [class-attribute](#class-attribute). Permissions as [class-attribute](#class-attribute) apply to all functions within the class.

### Unspecified resource

~~~php
<?php

#[Permission('read')]
~~~

### Specified resource

The second parameter can be used to specify the UUID of the resource. The UUID can, for example, be passed dynamically in the context of the REST API by means of a routing parameter.

~~~php
<?php

#[Permission('read', 'id')]
~~~

### Alternative context

The third parameter can be used to specify an alternative context so that policies from other apps can be checked.

~~~php
<?php

#[Permission('read', 'id', 'com.appsdock')]
~~~

### Multiple policies

Multiple policies can be passed directly as an array.

~~~php
<?php

#[Permission(['read', 'write', 'delete'])]
~~~

For specific resources or an alternative context, these must be listed separately.

~~~php
<?php

#[Permission(['read', 'write'])]
#[Permission('delete', 'id')]
#[Permission('administrate', context: 'com.appsdock')]
~~~

### Class attribute

~~~php
<?php

#[Permission('read')]
class DMS
{
	...
}
~~~

### Method attribute

~~~php
<?php

#[Permission('write')]
public function write(string $text): bool
{
...
}
~~~

### Special cases

!!! warning "Public access"
    Public access at class level can be overridden by policies at method level. Again, method-level public access ignores any additional policies.

~~~php
<?php

#[PublicAccess]
~~~

*[API]: Application Programming Interface
*[DMS]: Document Management System
*[REST]: Representational State Transfer
*[UUID]: Universally Unique Identifier

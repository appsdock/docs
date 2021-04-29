# Richtlinien und Berechtigungen

## Berechtigung

Eine Berechtigung besteht aus einer oder mehreren Richtlinien.

**Beispiel:**

Die Berechtigung *DMS-Anwender* hat das unbestimmte Recht innerhalb des gesamten DMS zu lesen und das bestimmte Recht in den eigenen Ordnern zu schreiben.

| Richtlinie | Aktion | Rolle | Ressource | Effekt
| ---------- | ------ | :---: | :-------: | :----:
| Lesen | com.appsdock.dms.action:read | *UUID* | ***\**** | ALLOW
| Schreiben | com.appsdock.dms.action:write | *UUID* | *UUID* | ALLOW

## Richtlinie

Eine Richtlinie besteht aus der Aktion, der Rolle, der Ressource und dem Effekt.

### Aktion

Aktionen werden von den Apps definiert.

**Beispiel:**

Die DMS-App definiert die Aktion *Ordner anlegen*.

### Rolle

Pro Richtlinie muss exakt eine Rolle zugewiesen werden.

### Ressource

Eine Ressource kann bestimmt oder unbestimmt sein. Unbestimmte Ressourcen werden mittels des ***\**** definiert.

### Effekt

Der Effekt ist entweder *Erlauben* oder *Verbieten*.

## Berechtigungssteuerung

Der Berechtigungssteuerung wird die Aktion als erster Parameter und der Kontext als zweiter Parameter angegeben.

~~~php
$isPermitted = $this->permissionController->isPermitted(
    'read',
    $this->context->getId()
);
~~~

Bei einer bestimmten Ressource wird deren *UUID* als dritter Parameter angegeben.

~~~php
$isPermitted = $this->permissionController->isPermitted(
    'read',
    $this->context->getId(),
    $appId
);
~~~

Alternativ kann ein Standardwert als vierter Parameter angegeben werden. Dieser wird nur zurückgegeben, wenn **keine** Richtlinie existiert.

~~~php
$isPermitted = $this->permissionController->isPermitted(
    'read',
    $this->context->getId(),
    $appId,
    $default
);
~~~

## REST API

Berechtigungen werden als [Methoden-Attribut](#methoden-attribut) oder alternativ als [Klassen-Attribut](#klassen-attribut) definiert. Berechtigungen als [Klassen-Attribut](#klassen-attribut) gelten für alle Funktionen innerhalb der Klasse.

### Unbestimmte Ressource

~~~php
#[Permission('read')]
~~~

### Bestimmte Ressource

Über den zweiten Parameter kann die *UUID* der Ressource angegeben werden. Die *UUID* kann bspw. im Kontext der REST API mittels eines Routing-Parameters dynamisch übergeben werden.

~~~php
#[Permission('read', 'id')]
~~~

### Alternativer Kontext

Über den dritten Parameter kann ein alternativer Kontext angegeben werden, damit man Richtlinien aus anderen Apps prüfen kann.

~~~php
#[Permission('read', 'id', 'com.appsdock')]
~~~

### Mehrere Richtlinien

Mehrere Richtlinien können direkt als Array übergeben werden.

~~~php
#[Permission(['read', 'write', 'delete'])]
~~~

Bei bestimmten Ressourcen oder einem alternativen Kontext müssen diese separat aufgeführt werden.

~~~php
#[Permission(['read', 'write'])]
#[Permission('delete', 'id')]
#[Permission('administrate', context: 'com.appsdock')]
~~~

### Klassen-Attribut

~~~php
#[Permission('read')]
class DMS
{
	...
}
~~~

### Methoden-Attribut

~~~php
#[Permission('write')]
public function write(string $text): bool
{
	...
}
~~~

### Sonderfall: *öffentlicher Zugriff*

Der öffentliche Zugriff auf Klassen-Ebene kann von Richtlinien auf Methoden-Ebene überschrieben werden. Wiederum ignoriert der öffentliche Zugriff auf Methoden-Ebene alle zusätzlichen Richtlinien.

~~~php
#[PublicAccess]
~~~

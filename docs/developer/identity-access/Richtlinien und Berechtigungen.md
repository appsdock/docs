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

### Code

Berechtigungen werden als Funktionsattribut angelegt. Berechtigungen welche für alle Funktionen gelten sollen können alternativ als Klassenattribut angelegt werden.

Berechtigungen beginnen immer mit dem Wort *Permission*, gefolgt von der Aktion in Klammern. Bei mehreren Aktionen werden diese als Array angegeben.

Standardmäßig werden Berechtigungen auf unbestimmte Ressourcen geprüft. Wenn bestimmte Ressourcen geprüft werden sollen, können diese als zweiter Parameter angegeben werden.

Berechtigungen werden standardmäßig im aktuellen Kontext geprüft. Soll eine Berechtigung in einem anderen Kontext geprüft werden, kann dieser als dritter Parameter angegeben werden.

~~~php
#[Permission('app.administrate')]
class AppWriteRestAPI extends RestAPIController
{​
    #[
        Permission(['app.extra', 'app.delete']),
        Permission('foo.bar', 'id'),
        Permission('bar.foo', context: 'com.appsdock')
    ]
    public function uninstall(string $appId): JsonResponse
    {
    	...
    }
}
~~~

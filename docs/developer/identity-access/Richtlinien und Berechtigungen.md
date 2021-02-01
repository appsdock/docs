# Richtlinien und Berechtigungen

## Berechtigung

Eine Berechtigung ist die logische Zusammenfassung von einer oder mehreren Richtlinien.

## Richtlinie

Eine Richtlinie besteht aus vier Teilen.

### Aktion

Aktionen werden von den Apps definiert.

**Beispiel:**

Die DMS-App definiert die Aktion *Ordner anlegen*.

### Identität

Identitäten sind entweder Rollen, Gruppen oder Benutzer.

### Ressource

Eine Ressource kann bestimmt oder unbestimmt sein.

**Beispiel:**

Ordner im DMS oder * für keine bestimmte Ressource bzw. alle Ressourcen.

### Effekt

Der Effekt ist entweder **Erlauben** oder **Verbieten**.

### Code

Berechtigungen werden als Funktionsattribut angelegt. Berechtigungen welche für alle Funktionen gelten sollen können als Klassenattribut angelegt werden. Berechtigungen beginnen immer mit dem Wort *Permission*, gefolgt von der Aktion in Klammern. Bei mehreren Aktionen werden diese als Array angegeben. Standardmäßig werden Berechtigungen auf unbestimmte Ressourcen geprüft. Wenn bestimmte Ressourcen geprüft werden sollen, können diese als zweiter Parameter angegeben werden. Berechtigungen werden standardmäßig im aktuellen Kontext geprüft. Soll eine Berechtigung in einem anderen Kontext geprüft werden, kann dieser als dritter Parameter angegeben werden.

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

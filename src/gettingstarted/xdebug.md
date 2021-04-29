# Phpstorm Xdebug-Einrichtung

* Deployment-Konfiguration des Vagrant Box vollenden
* Überprüfung der Einstellung siehe Screenshot

![Schritt 1](../assets/images/step1.png)

### Server einrichten

**Wichtig! Das Mapping Local-Path zu Remot Path (Bild Project Files)**

![Schritt 2](../assets/images/step2.png)

### Debugkonfiguration

Run -> Debug -> Edit Configurations -> Defaults aufklappen -> Php Remote Debug

Dort den in Schritt2 erstellten Server auswählen.

![Schritt 2](../assets/images/step3.png)

### Listening aktivieren

Run -> Start Listening for Php Connections


Dann Breakpoint setzen in Storm -> und Seite im Browser aufrufen et voila!!!

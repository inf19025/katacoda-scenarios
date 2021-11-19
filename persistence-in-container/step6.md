Bind Mounts sind direkte mounts, welche bei Docker mit Hilfe von absoluten oder relativen Pfaden angegeben werden. Bind Mounts werden nicht von Docker selbst verwaltet, weshalb in der Dokumentation von dem Benutzen jener abgeraten wird.

Um in unseren centos Docker Container einen lokalen Ordner zu mounten, benötigt es zu aller erst einen Lokalen Ordner. Diesen erstellen wir mit dem Befehl `mkdir mylocalvolume`{{execute}}.

Nachdem der Ordner erstellt wurde können wir wieder einen Docker Container starten und den lokalen Ordner dort verfügbar machen mit dem Befehl `docker run -it -v ./mylocalvolume:/mylocalvolume centos:latest`{{execute}}.

In dem Container können wir in useren Bind Mount mit `cd /mylocalvolume`{{execute}} navigieren. Der Befehl `echo "Test Datei in einem Bind Mount" >> test.txt`{{execute}} legt, wie zuvor, eine Test Datei an.

Mit `exit`{{execute}} können wir den Container wieder verlassen.

Weil der Ordner in unseren Verzeichnis liegt, können wir auf unserem Hostsystem mit `cd mylocalvolume`{{execute}} dort hinein navigieren. Mit dem Befehl `cat test.txt`{{execute}} können wir den Inhalt unserer Test Datei in der Konsole ausgeben.

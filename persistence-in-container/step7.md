Wie auch bei Volumes, können auch Bind Mounts in einer Docker Compose Datei genutzt werden.

Die unten beschriebene Datei, nutzt wieder einen bind mount. Auch hier nutzen wie wieder unseren lokalen Ordner `mylocalvolume`.<br>
Anders als bei dem `docker run` Befehl, kann hier ein relativer Pfad angegeben werden, welcher von dem Ordner der Datei aus geht. Dies ist zu sehen in den Definitionen der _volumes_ in der Datei.<br>

<pre class="file" data-filename="docker-compose.yml" data-target="replace">
version: '3.7'

services:
  centos: 
    image: centos:latest
    volumes:
      - ./mylocalvolume:/mylocalvolume
    command: docker
    stdin_open: true
    tty: true
</pre>

Den, in der Datei beschriebenen Container können wir wieder mit `docker-compose run centos /bin/bash`{{execute}} starten.

Mit dem Befehl `ls /mylocalvolume`{{execute}} können wir den Inhalt des Mounts sehen und mit `cat /mylocalvolume/test.txt`{{execute}} können wir den Inhalt unserer vorhin erstellten Datei ausgeben.

Um den Container wieder zu verlassen nutzen wir `exit`{{execute}}.

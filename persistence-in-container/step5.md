Docker Compose wird normalerweise genutzt um mehrere Container in einer lokalen Testumgebung zu nutzen. Es kann aber auch dazu dienen skalierbare Container mit Hilfe von Docker Swarm zu starten.

Auch hier können Docker Volumes genutzt werden, hierzu wird ein docker-compose.yml erstellt, welched mit dem Befehl `docker compose up` genutzt werden kann um die Container zu starten.

Wir benutzen wieder den centos container und nutzen unser vorhin erstelltes Volume _myvolume_, welches wir am Ende der Datei als _external_ markieren.<br/>
Zudem erstellen wir ein weiteres Volume, welches unter `/myvolume2` zu finden ist.

<pre class="file" data-filename="docker-compose.yml" data-target="replace">
version: '3.7'

services:
  centos: 
    image: centos:latest
    volumes:
      - myvolume:/myvolume
      - myvolume2:/myvolume2
    command: docker
    stdin_open: true
    tty: true

volumes:
  myvolume:
    external: true

  myvolume2:
</pre>

Um jetzt den Container, welchen wir im `docker-compose.yml` beschrieben habe zu starten benutzen wir `docker-compose run centos /bin/bash`{{execute}}.

Hier können wir in unser erstes Volume mit `ls /myvolume`{{execute}} hineinschauen und den Inhalt unser Test Datei mit `cat /myvolume/test.txt`{{execute}} ausgeben.

Zudem können wir in unser neues Volume mit `cd /myvolume2`{{execute}} navigieren.

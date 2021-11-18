Docker Compose wird normalerweise genutzt um mehrere Container in einer lokalen Testumgebung zu nutzen. Es kann aber auch dazu dienen skalierbare Container mit Hilfe von Docker Swarm zu starten.

Auch hier können Docker Volumes genutzt werden, hierzu wird ein docker-compose.yml erstellt, welched mit dem Befehl `docker compose up` genutzt werden kann um die Container zu starten.

Wir benutzen wieder den centos container und nutzen unser vorhin erstelltes Volume _myvolume_, welches wir am Ende der Datei als **external** markieren.<br/>
Zudem erstellen wir ein weiteres Volume, welches unter `/myvolume2` zu finden ist.

<pre class="file" data-filename="docker-compose.yml" data-target="replace">
  version: '3.7'

  services:
    db:
      image: centos:latest
      volumes:
        - myvolume: /myvolume
        - myvolume2: /myvolume2

  volumes:
    myvolume:
      external: true
    myvolume2:
</pre>

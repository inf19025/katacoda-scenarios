Wie auch bei Volumes, können auch Bind Mounts in einer Docker Compose Datei genutzt werden.

Die unten beschriebene Datei

<pre class="file" data-filename="docker-compose.yml" data-target="append">
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

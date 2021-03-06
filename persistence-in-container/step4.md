_Docker Volumes_ werden von Docker direkt verwaltet und der Nutzer muss keinerlei Speicherplatz direkt zuweisen.

# Volume anlegen

Um ein solches Volume anzulegen wird der Befehl `docker volume create {name}` genutzt.

Wir legen jetzt das Volume _myvolume_ mit dem Befehl `docker volume create myvolume`{{execute}}

# Volume testen

Zuerst können wir uns alle vorhandenen Docker Volumes mit `docker volume ls`{{execute}} anschauen.

Um unser Volume nun zu testen starten wir einen interaktiven Container mit dem _CentOS_ Image und mounten unseres Volume mithilfe der -v Flag in dem Pfad `/myvolume`.
`docker run -it -v myvolume:/myvolume centos:latest`{{execute}}

Nun ist unser Volume innerhalb des Containers, mit dem Pfad `/myvolume` vefügbar und wir können mit `cd /myvolume`{{execute}} dort hinein navigieren.

Mit dem Befehl `echo "Datei in myvolume" >> test.txt`{{execute}} erstellen wir die Datei _"test.txt"_ mit dem Inhalt "Datei in myvolume", den Inhalt der Datei können wir auch wieder mit dem Befehl `cat test.txt`{{execute}} ausgeben.

Abschliesend können wir unseren container wieder mit `exit`{{execute}} verlassen.

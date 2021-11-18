_Docker Volumes_ werden von Docker direkt verwaltet und der Nutzer muss keinerlei Speicherplatz direkt zuweisen.

# Volume anlegen

Um ein solches Volume anzulegen wird der Befehl `docker volume create {name}` genutzt.\
Wir legen jetzt das Volume _myvolume_ mit dem Befehl `docker volume create myvolume`{{execute}}

# Volume testen

Um unser Volume nun zu testen starten wir einen Container mit dem _CentOS_ Image.
`docker run -it centos:latest -v myvolume:/myvolume`{{execute}}

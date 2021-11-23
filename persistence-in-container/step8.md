Zum Schluss schauen wir uns noch einmal die von uns erstellten Docker Volumes an.

Mit dem Befehl `docker volume ls`{{execute}} geht genau dies.

Die Ausgabe listet alle von Docker verwalteten Volumes auf, also unser selbst erstelltes und das Volume, welches wir mit `docker compose` erstellt haben.

Hier ist anzumerken, dass der Befehl **nicht** unsere Bind Mounts anzeigt, da dieser nicht von Docker selbst verwaltet wird.

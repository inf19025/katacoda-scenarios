Container werden in der Softwareentwicklung genutzt um Anwendungen unabhägig von der Umgebung auszuführen. Die Unabhängigkeit von der Umgebung ist wünschenswert, damit inkompatible Abhängigkeiten die Anwendung nicht zum abstürzen bringen oder diese gar nicht erst startet.

# Funktionalität

Container fühlen sich ähnlich wie Virtuelle Maschinen an, wenn damit gearbeitet wird. Im Gegensatz zu Virtuellen Maschinen, bei welchen das gesamte Betriebssystem innerhalb eines Hostbetriebsystems virtualisiert wird, benutzen Container das Hostsystem für gewisse Funktionalitäten, wie Dateisysteme.

# Images

Container basieren auf sogenannten _Images_ welche eine Umgebung beschreiben in welcher gearbeitet werden kann. Hierbei ist es möglich ein eigenes Image zu beschreiben und zu bauen. Dies erlaubt es einem Entwickler, eine Anwendung samt benötigten Abhängigkeiten in einem eigenen Image zu verpacken. Diese Image kann im Anschluss in einem Zentralen Speicher gespeichert werden und ausgeführt werden. Das Image Format ist Standardisiert und kann deshalb von vielen verschiedenen

# Docker

Die am weitest verbreitete, sogenannte _Container Engine_ ist Docker. Daher wird in diesem Tutorial am stärksten auf Docker eingegangen.

Container werden in der Softwareentwicklung genutzt um Anwendungen unabhägig von der Umgebung auszuführen. Die Unabhängigkeit von der Umgebung ist wünschenswert, damit inkompatible Abhängigkeiten die Anwendung nicht zum abstürzen bringen oder diese gar nicht erst startet.

# Funktionalität

Container fühlen sich ähnlich wie Virtuelle Maschinen an, wenn damit gearbeitet wird. Im Gegensatz zu Virtuellen Maschinen, bei welchen das gesamte Betriebssystem innerhalb eines Hostbetriebsystems virtualisiert wird, benutzen Container das Hostsystem für gewisse Funktionalitäten, wie Dateisysteme.

# Images

Container basieren auf sogenannten _Images_ welche eine Umgebung beschreiben in welcher gearbeitet werden kann. Hierbei ist es möglich ein eigenes Image zu beschreiben und zu bauen.

# Docker

Die am weitest verbreitete, sogenannte _Container Engine_ ist Docker. Daher wird in diesem Tutorial am stärksten auf Docker eingegangen.

# Podman

Eine, auf dem Desktop, weit verbreitete Alternative zu Docker ist Podman. In Produktivumgebungen wird Podman weniger verwendet, da es Benutzerunfreundlicherere, dafür leichtere Alternativen gibt.

# System-Programmierung
## Hands-on zu Lektion 11
Für Slides und Code Beispiele, siehe [Lektion 11](../../../fhnw-syspr/blob/master/11/README.md)

> *Achtung: Arbeiten Sie nicht direkt auf diesem Repository.*<br/>
> *[Erstellen Sie eine persönliche Kopie, mit diesem GitHub Classroom Link](https://classroom.github.com/a/GNdhwGxy).*

### a) Kalender-Zeit, 5'
* Lesen Sie das folgenden [TLPI](http://man7.org/tlpi/) Beispiel Programm:<pre>
[calendar_time.c](http://man7.org/tlpi/code/online/book/time/calendar_time.c.html)</pre>
* Vergleichen Sie den Output der Kommandos:<pre>
    $ ./date
    $ ./calendar_time</pre>

### b) Zeit parsen / formatieren, 5'
* Lesen Sie das folgenden [TLPI](http://man7.org/tlpi/) Beispiel Programm:<pre>
[strtime.c](http://man7.org/tlpi/code/online/book/time/strtime.c.html)</pre>
* Vergleichen Sie den Output der Kommandos:<pre>
    $ ./strtime "9:39:46pm 1 Feb 2011" "%I:%M:%S%p %d %b %Y"
    $ ./strtime "9:39:46pm 1 Feb 2011" "%I:%M:%S%p %d %b %Y" "%F %T"</pre>
* Geben Sie das Datum im [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) Format aus.

### c) Zeitmessung, 15'
* Schreiben Sie ein eigenes *time* Programm, *my_time.c*
* Das zu messende Programm soll aus *argv* gelesen und mit *fork()* und *execve()* gestartet werden.
* Der Parent Prozess wartet mit *wait()*, und bestimmt die Laufzeit, real und CPU Zeit, des Child Prozesses.
* Die Ausgabe soll derjenigen von *time* entsprechen.

### d) Timer, 5'
* Lesen Sie das folgenden [TLPI](http://man7.org/tlpi/) Beispiel Programm:<pre>
[real_timer.c](http://man7.org/tlpi/code/online/book/timers/real_timer.c.html)</pre>
* Testen Sie den Timer, z.B. mit den Kommandos:<pre>
    $ ./real_timer 1 800000 1 0 # 1.8s, 1s Periode
    $ ./real_timer 3 0 # einmaliger Timer, nach 3s</pre>

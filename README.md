# Volleyballturnier
Dies ist die offizielle Repository für das Volleyball-Website.
Hier findet man die wichtigen Dateien für die Website, wie die HTML und CSS-Dateien zur Ansicht der Website.

# Wichtige Hinweise
  
           


<ul>
  <li>Die Webseite wurde für Smartphones entwickelt. UI-Elemente werden auf dem Tablet oder PC anders auftauchen, als sie intentionell designed wurden.</li>
  <li>Auf dieser Webseite gibt es keine Sicherheitsmaßnahmen und bei Spamversuchen oder DDoS-Attacken werden wichtige Elemente wie URL-Eingabe und Buttons vom UI entfernt!</li>
  <li>Auf der HTML-Seite befinden sich wichtige API-Elemente, um die Nutzung der Datenbank zu ermöglichen. Diese werden bewusst an jeden (unsichtbar) bekannt gemacht und bei fälschlichem Gebrauch, wird konsequent die Songanfrage gesperrt.</li>
</ul> 

## Frontend
Es gibt viele interessanten Mechanismen hinter der Webseite, die bewusst im Vordergrund nicht gezeigt werden.        

### Spielplan
Es fängt schon mit dem Spielplan an.
Wir nutzen die Seite tournify.de um den Spielplan zu zeigen. Wir haben uns eine Lizenz für 40€ erworben, um die volle Funktion nutzen zu können. 
Dazu haben wir es auf die Webseite mit der folgenden Funktion implementiert:

```html
<iframe id="plan" src="https://www.tournify.de/live/gsgd-colleyballturnier/standings"></iframe>
```

Dies ermöglicht uns, eine komplette Seite anzeigen zu lassen, ohne irgendwelche großen Einschränkungen.
Es gibt jedoch eine Sache, die mich besonders nervt.

Bei der CSS-Datei gibt es das Attribut overscroll-behavior.
```css
#plan{
        height: 650px;
        width: 400px;
        border-radius: 15px;
        overscroll-behavior: hidden;
    }
```
Dies ist eine Eigenschaft, in der man vorgeben kann, was passieren soll, wenn das Bild größer ist als das Fenster.Sprich, wenn wir ein Bild in Größe 15x15cm haben aber der Rahmen nur 10x10cm groß ist. 

### Spotify


Die restliche Seite wurde mit den Standartblöcken von HTML designed. Also gibt es nichts spezielles oder aufregendes mehr.

## Backend
Im Hintergrund arbeiten zwei wichtige Systeme, die miteinander verbunden sind und nur miteinander arbeiten.
Wir haben eine Datenbank und einen Pythonscript, der lokal auf einem Computer läuft und ein Mensch zu jederzeit die Übersicht hat. Diese Systeme sind nur für die Songvorschläge zuständig.

### Datenbank
Die Datenbank ist von Firebase, welches von Google betrieben wird. Jeder Songvorschlag wird mithilfe der Webseite zur Datenbank weitergeleitet und dabei werden nur zwei entscheidende Daten gespeichert:
<ol>
  <li>Zeitstempel</li>
  <li>Song-URL</li>
</ol> 
Diese werden anonymisiert an die Datenbank, welches sich in der EU befindet, gesendet und somit braucht man keine Datenschutzerklärung.

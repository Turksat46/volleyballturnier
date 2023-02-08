# Volleyballturnier
Dies ist die offizielle Repository für das Volleyball-Website.
Hier findet man die wichtigen Dateien für die Website, wie die HTML und CSS-Dateien zur Ansicht der Website.

## Backend
Es gibt viele interessanten Mechanismen hinter der Webseite, die bewusst im Vordergrund nicht gezeigt werden. Es fängt schon mit dem Spielplan an.
Wir nutzen die Seite tournify.de um den Spielplan zu zeigen. Wir haben uns eine Lizenz für 40€ erworben, um die volle Funktionen nutzen zu können. 
Dazu haben wir es auf die Webseite mit der folgenden Funktion implementiert:

```html
<iframe id="plan" src="https://www.tournify.de/live/gsgd-colleyballturnier/standings"></iframe>
```

Dies ermöglicht uns, eine komplette Seite anzeigen zu lassen, ohne irgendwelche großen Einschränkungen.
Es gibt jedoch eine Sache, die mich besonders nervt.

Bei der CSS-Datei gibt es das Attribut 
```css
#plan{
        height: 650px;
        width: 400px;
        border-radius: 15px;
        overscroll-behavior: hidden;
    }
```

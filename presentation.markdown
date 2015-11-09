class: s s-center c-title
background-image: url(images/escher-spiral-cropped.jpg)

.c-title--headline[
# ECMAScript 6
### Die neueste Version von JavaScript
]

.c-title--meta[
.c-title--author[
  Paul Kögel, M.A.
]
.c-title--links[
  [@wakkahari](https://twitter.com/wakkahari) &ndash; <paul@railslove.com>
]
]

.c-title--note[
  'p' drücken, um Präsentationsnotizen ein-/auszublenden]

---

class: s s-center s_background-grey
background-image: url(images/paul_kogel_wakkahari.jpg)

.full-page-link[
[](https://twitter.com/wakkahari)
]

???
+ kurz vorstellen: Entwickler bei **Railslove**: Webfrontends mit JavaScript, Ruby und Clojure

---

+ Lust auf Programmieren machen
+ dieser Vortrag: kritische 
+ neue

---

class: s s-center

# <u>Java</u>Script ≠ <u>Java</u>

???
+ fangen wir von ganz außen an
+ das Wichtigste, was man über JavaScript wissen muss

---



class: s s-center

## Warum JavaScript?

.c-list.u-width-70[
+ nicht wegen Eleganz oder Robustheit
  - .text-red[**eher bekannt für Brüchigkeit**]
  - trotzdem .text-green[**schöner Kern**], der durch ES6 noch schöner wird
+ Sprache des Webs -> viele Entwickler
+ heute .text-green[**allgegenwärtig**], wird so schnell nicht mehr verschwinden
]

???
+ allgegenwärtig: Browser, Server (Node.js), Datenbanken (Mongo, Couch, ...), Roboter (Nodecopter), Photoshop Plugins, Windows Apps, Native Apps (React Native).

---

class: s s-center

## In einem Bild
.u-width-70[
![](images/javascript-good-bad-parts.jpg)
]

???
klassische Metapher für JavaScript
im linken Buch steht alles über JavaScript
das rechte Buch bekommt man, wenn man die ganzen Sachen, die an JavaScript schlecht sind, aus dem dicken Buch herausreißt.

---

class: s s-center

## ...und in noch einem

![If JavaScript were a weapon: sword without a hilt](images/javascript-weapon.png)
.text-center.text-mini[
Quelle: [If programming languages were weapons](http://bjorn.tipling.com/if-programming-languages-were-weapons)
]

???
aktualisiert

---

class: s s-center

# ECMAScript 6 =<br> Lederhandschuh für JavaScript

???
+ durchkommen der Zacken lässt sich nicht vermeiden (Abwärtskompatibilität), aber man kann jetzt besser an den weniger spitzen Stellen seine Finger ablegen, um das Schwert zu halten

---

class: s s-center

# Inhalt

.row.u-full-width.c-inhalt--list[
.col.col-50[
1. Orientierung & **Hintergrund**
  + Begrifflichkeiten
  + Ursprünge von JS
  + .text-green[**Aufstieg**]
  + .text-red[**Probleme**]
  + Motivation für ES6
]

.col.col-50.c-inhalt--ol-with-counter[
2. **ES6 Praxis**
  + Sprachfeatures
  + Nutzung mit Transpiler Babel
3. Ausblick
  + ES7
]
]

---

class: s s-center

# Nicht

+ kein vollständiger Überblick

???
+ ES6 hat zu viele neue Features, als das man sie alle in anderthalb Stunden vorstellen könnte

---

class: s s-center s_no-padding s_background-grey c-garden-bosch
background-image: url(images/hieronymus-bosch-the-garden-of-earthly-delights-crop.jpg)

.s--headline-overlay[
# 1. Orientierung
]

???
Dschungel von Namen, ständig neue Entwicklungen

---

class: s s-center


# Motivation

"Netscape also wanted a lightweight interpreted language that would complement Java by appealing to nonprofessional programmers, like Microsoft's Visual Basic"
http://ghost.jollygoodthemes.com/toffee/the-story-of-javascript/

---

class: s s-center

# JavaScript: 1995-...

.row[
.col.col-33[
### Brendan Eich
![Brendan Eich](images/brendan-eich.jpg)
.text-tiny.text-grey-inherit[
<br><br>
Quelle: Darcy Padilla  
[http://web.archive.org/web/20140209081556/http://blog.mozilla.org/press/bios/brendan-eich](http://web.archive.org/web/20140209081556/http://blog.mozilla.org/press/bios/brendan-eich)
]]

.col.col-33[
### &nbsp;
![Netscape](images/netscape-logo.svg)
<br><br>
![Sun Microsystems](images/sun-logo.svg)
]


.col.col-33[
### Namen
+ (Mocha)
+ (LiveScript)
+ **JavaScript**
]
]

???
+ 1995 von Brendan Eich erschaffen
+ Netscape: damals einer der populärsten Browser, später open source und daraus entstand die Mozilla Foundation die heute Firefox herausgibt
+ missverständlicher Name: Java war sehr hip, Kooperation zwischen Netscape und **Sun**, der Firma hinter Java (später von Oracle gekauft)
+ 8.-populärste Programmiersprache Sprache (vgl.: [http://www.heise.de/developer/meldung/Programmiersprachen-Top-10-Objective-C-raus-Ruby-wieder-rein-2837323.html](http://www.heise.de/developer/meldung/Programmiersprachen-Top-10-Objective-C-raus-Ruby-wieder-rein-2837323.html))

---

class: s s-top

.u-width-70.text-center[

.u-width-70.u-center[
![](images/office-space-done-1-crop.jpg)
]
<br>
.u-no-margin[
### .text-normal[Die wesentlichen Teile von JavaScript wurden in]

# 10 Tagen

### .text-normal[geschrieben.]
]
]

---

class: s s-top

.u-width-70.text-center[

.u-width-70.u-center[
![](images/office-space-done-2-colours.jpg)
]
<br>
.u-no-margin[
### .text-normal[Die wesentlichen Teile von JavaScript wurden in]

# 10 Tagen

### .text-normal[geschrieben.]
]
]

.u-margin-top-20.u-background-red.text-white.u-border-radius-10.u-padding-10[
.u-no-margin[
...und lassen sich nicht mehr ändern &#9785;
]
]

???
+ Hier liegt der Hund begraben
+ Abwärtskompatibilität

---

class: s s-top

## Beispiel: `==` (lose Gleichheit)

```javascript
'0' == 0     // true
 0  == ''    // true
'0' == ''    // false
```

--

`==` ist .text-red[**nicht transitiv**], da aus
```javascript
a == b
b == c
```
_nicht_ folgt, dass `a == c`

???
+ lose Gleichheit: nach Typenkonvertierung
+ `==` ist **kommutativ** (Seiten vertauschbar) aber **nicht transitiv** (wenn `a==b` und `b==c` folgt daraus nicht immer, dass auch `a==c`)
+ **Brendan Eich** wollte schon früh `==` sich wie heutiges `===` verhalten lassen - war allerdings schon in JS 1.2 zu spät :(

**weitere Beispiele:**
```javascript
false == '0'        // true
false == undefined  // false
false == null       // false
null == undefined   // true

'      ' == 0 // true     
'\n\r\t' == 0 // true
```

Quellen:
http://www.shawnrenner.com/the-dangers-of-double-equals-in-javascript/
http://stackoverflow.com/a/359509/1881819

---

class: s s-center

# Draufspachteln
.c-list.u-width-70[
+ Semantik von `==` lässt sich nicht mehr ändern, da bestehender Code davon abhängt
+ `===` (strikte Gleichheit) hinzugefügt.

+ Noch gröbere Schnitzer werden aus der Sprache entfernt: früher ließ sich `undefined` überschreiben.
]  

???
+ `===` schaut sich `typeof` noch an.
+ `NaN === NaN` gibt `false`
+ auf die Variable von `var undefined` wird nicht zugegriffen sondern immer nur auf das echte undefined. `var undefined` wirft keinen Fehler.

---

class: s s-center

.text-quote.text-medium[
“I perpetrated JavaScript ...”
]
.text-quote--author.text-small[
\- Brendan Eich, JavaScript Jabber Podcast
]

---

background-image: url(images/eminem-c-hammer.jpg)

???
+ passendste Metapher - gerade im Hinblick auf ES6: Man hat Eminem und der kann nicht gut genug rappen. Dann fängt man an MC Hammer drüberzukleistern und es sieht immer mehr wie n richtiger Rapper aus, aber immer wieder scheint dieser Eminem durch.

ES6: großer Schritt n anständiger Rapper, eine solide Programmiersprache zu werden - nichts gegen Eminem.

---



# Heute
+ JavaScript in/auf
  - Browsern
  - Servern
  - Datenbanken
  - Windows
  - native Apps
  - ...
+ Full-Stack JavaScript Entwickler

???
full stack: Frontend, Backend (nodeJS), Datenbank (Mongo, CouchDB)
http://javascript.crockford.com/popular.html

---

"JavaScript is the only language that I’m aware of that people feel they don’t need to learn before they start using it."

---

background-image: url(images/old-people.jpg)

---

nicht totzukriegen
https://brendaneich.github.io/ModernWeb.tw-2015/images/alwaysbetonjs.png

---

class: s s-center

#Übersicht

.row[
.col.col-33[
### Sprache
+ .text-green[**JavaScript**]
]

.col.col-33[
### Standard
+ .text-green[**ECMAScript**]
+ TC39 Komitee
]

.col.col-33[
### Versionen
+ ES 5.1
+ .text-green[**ES 6**]<sup>th</sup> Ed. / ES 2015 / Harmony
+ ES7
]
]

???
erste Version in Netscape 2 Beta, 1995
Standardisiert: 1997

+ ES5.1: in Browsern gerade eingebaut
+ ES6: seit Juni 2015 standardisiert, wird gerade eingebaut
+ ES7: kommt bald

### Sprache
+ Netscape
Mocha, Marketing: LiveScript -> JavaScript
März 1996: version 1 in Netscape Navigator 2.0 / InternetExplorer 3.0

### Standard
+ **E**uropean **C**omputer **M**anufacturers **A**ssociation, hat auch die CD-ROM standardisiert
+ durften den namen JavaScript nicht benutzen für den Standard
+ erste Version: Juni 1997
+ Version seit 2009, 5.1 (in heutigen Browsern) seit 2011
+ ES6 seit Juni 2015

+ [Übersicht der ECMAScript Versionen](https://en.wikipedia.org/wiki/ECMAScript#Versions)
+ [JavaScript - ECMAScript Versionsensprechungen](https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence)

---

class: s s-center

# Implementierungen

+ Mozilla: JavaScript
+ Microsoft: JScript
+ Adobe: ActionScript, AcrobatScript

# JavaScript Engines

+ [Spidermonkey](https://en.wikipedia.org/wiki/SpiderMonkey_%28software%29) (Mozilla)
+ [v8](https://en.wikipedia.org/wiki/V8_%28JavaScript_engine%29) (Chrome, node.js)
+ [JavaScript Core](https://en.wikipedia.org/wiki/WebKit#JavaScriptCore) ("Nitro", Safari)
+ Chakra (Microsoft)
+ [...](https://en.wikipedia.org/wiki/JavaScript_engine)


???
+ Implementierungen / Interpreter / VMs
+ [JS Engines](https://en.wikipedia.org/wiki/JavaScript_engine) sind VMs in denen JS ausgeführt wird.
+ [JavaScript Core]

(BONUS)
+ Spidermonkey-Versionen = JavaScript versionen, heute: version 31, 2011: 1.8.5, März 1996: 1.0

---

Eternal JavaScript
einzige Sprache, die in Browsern eingebaut ist
überall eingebaut
Geschichte
https://en.wikipedia.org/wiki/JavaScript_engine#The_JavaScript_engine_race:_2008_and_2009

---

workarounds vor ES6: jQuery, Underscore.js, JSHint, Babel Warnungen

---


https://kangax.github.io/compat-table/es6/

asm.js, emscripten,
compile to JS languages (CoffeeScript, ClojureScript, Dart, Typescript, PureScript, Elm, ...)


---
ES6 Features
+ Promises
+ Klassen
bei beiden: davor Chaos, viele verschiedene Implentierungen

ES6 macht den Einstieg leichter, man braucht weniger Libraries wie underscore.JS oder jQuery

---

# Ausblick

+ ES6 ist n Lederhandschuh, 

---


Dokumentation:
https://developer.mozilla.org/en/docs/Web/JavaScript

[CologneJS](http://colognejs.de)


Links:
https://brendaneich.github.io/ModernWeb.tw-2015/
https://shaunlebron.github.io/solar-system-of-js




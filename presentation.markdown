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

???
ECMAScript 6 (ES6): aktuelle Version von JavaScript
JavaScript: Sprache für Datepicker

---

class: s s-top s_background-grey s_background-50 s_background-bottom
background-image: url(images/paul-kogel.jpg)

# Paul Kögel
+ Frontends bei [.text-green[Railslove]](http://railslove.com)
+ JavaScript, Ruby, Clojure
+ [@wakkahari](https://twitter.com/wakkahari)


???
+ kurz vorstellen: Entwickler bei **Railslove**: Webfrontends mit JavaScript, Ruby und Clojure

---

class: s s-top s_background-bottom s_background-30
background-image: url(images/dilbert-lunch-cut.png)

# Themen

.row.u-full-width.c-inhalt--list[
.col.col-50.u-no-padding-left[
1. **Hintergrund**
  + Begrifflichkeiten
  + Geschichte
  + Probleme
  + Motivation für ES6
]

.col.col-50.c-inhalt--ol-with-counter[
2. **ES6 Praxis**
  + Sprachfeatures
  + Nutzung mit Transpiler Babel
3. Ausblick
  + ES7
  + Assembler des Webs
]
]

???
+ beginnen mit Erklärung der Namen - warum heißt das ausgerechnet JavaScript und warum heißen Versionen davon ECMAScript?
+ dann schauen wir uns JavaScripts Geschichte an: Entstehung und Aufstieg
+ Reisewarnung für Gefahrenzone
+ schließlich zeig ich euch Probleme, die großer Teil der Motivation für ES6 waren

+ im **2. Teil**

---

class: s s-center s_no-padding s_background-cover
background-image: url(images/death-star-briefing.png)

.s--headline-overlay[
# 1. Hintergrund
]

---

background-image: url(images/catbert.png)
class: s s-top s_background-bottom s_background-30
<br>
<br>
# <u>Java</u>Script ≠ <u>Java</u>

???
+ das Wichtigste am Anfang
+ haben nichts miteinander zu tun
+ werden gleichs sehen wie es zu dem unglücklichen Namen kommt

---

background-image: url(images/javascript-logo.jpg)
class: s s-top s_background-20 s_background-bottom

## „Sie wollen also JavaScript schreiben...“

.c-list.u-width-70[
+ nicht bekannt für besondere Eleganz oder Robustheit
  - eher für .text-red[**Brüchigkeit**] und .text-red[**böse Überraschungen**]
  - dennoch _kann_ man .text-green[**elegante Programme**] schreiben
+ .text-green[**Sprache des Webs**]
+ .text-green[**schnell sichtbare Ergebnisse**]
+ .text-green[**allgegenwärtig & universell**]
]

???
+ warum schauen wir uns JS an?
+ Eleganz: durch ES6 noch verbessert
+ .text-green[Sprache des Webs]: viele Zielgeräte, viele Entwickler
+ **allgegenwärtig**: Browser, Server (Node.js), Datenbanken (Mongo, Couch, ...), Roboter (Nodecopter), Photoshop Plugins, Windows Apps, Native Apps (React Native).
+ **universell**: man kann damit heute fast alles schreiben und die Möglichkeiten wachsen
+ **Full-Stack JavaScript Entwickler**

---

class: s s-top s_background-bottom s_background-50
background-image: url(images/office-space-lumberg-hmmm.jpg)

```javascript
Math.max();
// -Infinity

Math.min();
// Infinity
```

.text-mini[
<br>
mehr: [wtfjs.com](http://wtfjs.com)
]

???
+ nichts was einem jeden Tag begegnet
+ gibt Beispiele mit denen Firmen Hunderttausende von Dollar verloren haben :(

---

class: s s-center

```javascript
var a = [];
var b;
a[b++] = 1;
```

.text-mini[
Quelle: [Type safety and RNGs](https://medium.com/@octskyward/type-safety-and-rngs-40e3ec71ab3a)
]

???
+ b ist `undefined`
+ `undefined++` gibt `NaN`
+ a[NaN] verändert a nicht, wirft aber auch keinen Fehler

---

class: s s-top

## JavaScript in einem Bild
.u-width-70[
![](images/javascript-good-bad-parts.jpg)
]

???
klassische Metapher für JavaScript
im linken Buch steht alles über JavaScript
das rechte Buch bekommt man, wenn man die ganzen Sachen, die an JavaScript schlecht sind, aus dem dicken Buch herausreißt.

---

class: s s-top

## ...

![If JavaScript were a weapon: sword without a hilt](images/javascript-weapon.png)
.text-center.text-mini[
Quelle: [If programming languages were weapons](http://bjorn.tipling.com/if-programming-languages-were-weapons)
]

???
+ Schwert ohne Griff, bei dem man sich unweigerlich blutige Finger holt

---

class: s s-top s_background-bottom
background-image: url(images/leather-gloves.jpg)

<br>
<br>
# ECMAScript 6 =<br> Lederhandschuhe für JavaScript

???
+ durchkommen der Zacken lässt sich nicht vermeiden (Abwärtskompatibilität), aber man kann jetzt besser an den weniger spitzen Stellen seine Finger ablegen, um das Schwert zu halten

---

class: s_background-cover
background-image: url(images/office-space-lumbergh.jpg)

.u-background-green.text-white.u-width-50.u-padding-20.u-no-margin-vertical.u-border-radius-10[
JavaScript ist trotzdem **super**!
]

???
+ lieber als Ruby, obwohl das die sauberere Sprache ist
+ ich schreib gerne JavaScript weil im Browser & allen zeigbar und gut geeignet für funktionale Programmierung / sich hier gerade sehr viel tut mit guten Ideen wie man Frontends bauen kann.
+ normalerweise werden bei Vorträgen zu neuen Sprachversionen nur die Vorteile hervorgehoben und keiner fragt, woran es denn liegt, dass all diese Verbesserungen notwendig waren
+ ES6 ist nicht der Weisheit letzter Schluss, ES7 ist schon in der Mache
+ zeigen warum überhaupt ES6 / Motivation dahinter und Beispiel zeigen wie Programmiersprachen sich über die Zeit entwickeln.

---

class: s s-center

BEI PRAXISTEIL AM ANFANG SAGEN
# Nicht

+ kein vollständiger Überblick

???
+ ES6 hat zu viele neue Features, als das man sie alle in anderthalb Stunden vorstellen könnte

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

class: s s-center

# Babel

`npm install -g babel-cli`

---

# Ausblick

+ ES6 ist n Lederhandschuh, ClojureScript etc. ist n richtiges Schwert mit Griff
+ ES7 ist in der Mache - soll 2016 kommen
+ Aufnahmeprozess neuer Features ist durch Entwicklergemeinde mitgesteuert, mit Babel kann man früh Feedback zu vorgeschlagenen Syntaxerweiterungen bekommen

---

Dokumentation:
https://developer.mozilla.org/en/docs/Web/JavaScript

[CologneJS](http://colognejs.de)


Links:
https://brendaneich.github.io/ModernWeb.tw-2015/
https://shaunlebron.github.io/solar-system-of-js

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
background-image: url(images/p/dilbert-lunch-cut.png)

# Themen

.row.u-full-width.c-inhalt--list[
.col.col-50.u-padding-left-100[
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
background-image: url(images/p/death-star-briefing.jpg)

.s--headline-overlay[
# 1. Hintergrund
]

---

background-image: url(images/p/catbert.png)
class: s s-top s_background-bottom s_background-30
<br>
<br>
# <u>Java</u>Script ≠ <u>Java</u>

???
+ das Wichtigste am Anfang
+ haben nichts miteinander zu tun
+ werden gleichs sehen wie es zu dem unglücklichen Namen kommt

---

class: s s-center

## Ursprung: 1995

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
+ Mocha, Marketing: LiveScript &rArr; JavaScript

---

class: s s-top s_background-30 s_background-bottom-with-padding
background-image: url(images/netscape-logo.svg)

## Netscapes Ziel

.c-list[
+ leicht zugänglich für Amateure
  - interpretiert & untypisiert
  - Vorbild: Visual Basic
  - in HTML einbettbar
+ als einfachere Ergänzung zu Java gedacht
]

???
+ leicht zugänglich: kein Kompilierungsschritt, keine Typen, man kann Code aus verschiedenen Quellen zusammenbasteln (copy & paste)

Quellen:
+ JavaScript Jabber withb Brendan Eich
+ http://ghost.jollygoodthemes.com/toffee/the-story-of-javascript

---

class: s s-top s_no-padding

## Standardisierung für viele Dialekte

<table>
  <thead>
    <tr>
      <td>Jahr</td>
      <td>JavaScript</td>
      <td>JScript</td>
      <td>ECMAScript</td>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1996</td>
      <td>1.0 (Netscape 2.0)</td>
      <td>1.0 (IE 3.0)</td>
      <td>--</td>
    </tr>
    <tr>
      <td>1997/98</td>
      <td>1.3</td>
      <td>3.0</td>
      <td>Ed.1 / Ed. 2</td>
    </tr>
    <tr>
      <td>1999</td>
      <td>1.5</td>
      <td>5.5</td>
      <td>"</td>
    </tr>
    <tr>
      <td>2008</td>
      <td>1.8 (Gecko 1.9)</td>
      <td>5.6</td>
      <td>Ed. 3</td>
    </tr>
    <tr>
      <td class='text-red'><b>eingestellt</b></td>
      <td>"</td>
      <td>"</td>
      <td>ES4</td>
    </tr>
    <tr>
      <td>2009</td>
      <td>"</td>
      <td>"</td>
      <td>ES5</td>
    </tr>
    <tr>
      <td>2011</td>
      <td>"</td>
      <td>"</td>
      <td>ES5</td>
    </tr>
    <tr>
      <td>2015</td>
      <td>"</td>
      <td>"</td>
      <td>ES6</td>
    </tr>
    <tr>
      <td>2015</td>
      <td>?</td>
      <td>?</td>
      <td>ES7</td>
    </tr>
  </tbody>
</table>

???
+ rechte Spalte zeigt ECMAScript Versionen
+ ES = Standard für JavaScript
+ heißt anders, da dafür die Lizenz von Sun nicht genutzt werden durfte
+ **E**uropean **C**omputer **M**anufacturers **A**ssociation, hat auch die CD-ROM standardisiert
+ durften den namen JavaScript nicht benutzen für den Standard
+ erste Version: Juni 1997

JScript: Microsoft's JavaScript Dialekt, daneben gibt's noch 
Browser Wars: Vorwürfe, dass Netscape seine Erfinderrolle zum eigenen Vorteil nutzt &rArr; Standardisierung war wichtig

Quellen:  
[https://en.wikipedia.org/wiki/JavaScript#Version_history](https://en.wikipedia.org/wiki/JavaScript#Version_history)  
[https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence](https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence)  
[https://en.wikipedia.org/wiki/ECMAScript#Versions](https://en.wikipedia.org/wiki/ECMAScript#Versions)

---

class: s s-top s_background-35 s_background-bottom
background-image: url(images/jagermonkey.jpg)

# JavaScript Engines
+ [Spidermonkey](https://en.wikipedia.org/wiki/SpiderMonkey_%28software%29) (Mozilla)
+ [v8](https://en.wikipedia.org/wiki/V8_%28JavaScript_engine%29) (Chrome, Node.js)
+ [JavaScript Core](https://en.wikipedia.org/wiki/WebKit#JavaScriptCore) ("Nitro", Safari)
+ Chakra (Microsoft)
+ [... 10 mehr](https://en.wikipedia.org/wiki/JavaScript_engine)

???
+ Implementierungen innerhalb eines Herstellers / Interpreter / VMs
+ [JS Engines](https://en.wikipedia.org/wiki/JavaScript_engine) sind VMs in denen JS ausgeführt wird.

(BONUS)
+ [https://en.wikipedia.org/wiki/JavaScript_engine#The_JavaScript_engine_race:_2008_and_2009](https://en.wikipedia.org/wiki/JavaScript_engine#The_JavaScript_engine_race:_2008_and_2009])

---

class: s s-center s_background-20 s_background-bottom
background-image: url(images/p/dogbert.jpg)

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
+ .text-green[**ES 6**]<sup>th</sup> Ed. / **ES 2015** / Harmony
+ ES7
]
]

???
**TC39**: Gremium mit Vertretern aus der Industrie, Mozilla, Freiwillige

für uns **relevante Versionen**
+ ES5.1: in Browsern gerade eingebaut
+ ES6: seit Juni 2015 standardisiert, wird gerade eingebaut
+ ES7: kommt bald

### Standard
+ Version seit 2009, 5.1 (in heutigen Browsern) seit 2011
+ ES6 seit Juni 2015

+ [Übersicht der ECMAScript Versionen](https://en.wikipedia.org/wiki/ECMAScript#Versions)
+ [JavaScript - ECMAScript Versionsensprechungen](https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence)

---

class: s s-top

## JavaScripts Aufstieg

.c-list[
+ **Ende der 90er**:
  - kleine Skripte
  - Java Applets
+ **1998**: Mozilla, Netscape an AOL verkauft
+ **2005**: Ajax
+ **2006**: jQuery
+ **2007**: iPhone &rArr; Flash auf dem Rückzug
+ **2008**: Google Chrome &amp; v8
+ **2009**: Node.js, ES5
]

???
TIOBE Index vgl.: [http://www.heise.de/developer/meldung/Programmiersprachen-Top-10-Objective-C-raus-Ruby-wieder-rein-2837323.html](http://www.heise.de/developer/meldung/Programmiersprachen-Top-10-Objective-C-raus-Ruby-wieder-rein-2837323.html)

---

class: s s-top s_no-padding s_background-bottom s_background-50
background-image: url(images/full-stack-homer.jpg)

.u-no-margin-bottom[
## JavaScript 2015:
]

+ 8.-populärste Programmiersprache
+ Flash tot, JS konkurrenzlos!?
+ Wirtschaft mag 1 Sprache

???
full stack: Frontend, Backend (nodeJS), Datenbank (Mongo, CouchDB)

(BONUS)
[The World's Most Misunderstood Programming Language Has Become the World's Most Popular Programming Language](http://javascript.crockford.com/popular.html)

---

class: s s-center s_background-green
background-image: url(images/aliens-javascript.jpg)

???
+ also alles super, wir gehen die neuen Features von ES6 durch und uns haut's alle aus den Socken

---

class: s s-center s_no-padding s_background-cover
background-image: url(images/p/island-storm.jpg)

.s--headline-overlay[
# Probleme
]

---

class: s s-top s_background-blue

.u-width-70.text-center[

.u-width-70.u-center[
![](images/office-space-done-1-crop.jpg)
]
<br>
.u-no-margin[
### .text-normal[JavaScript 1.0 wurde in]

# 10 Tagen

### .text-normal[geschrieben.]
]
]

???
+ was erstmal wie ne stramme Leistung von Brendan Eich klingen mag...

---

class: s s-top s_background-red

.u-width-70.text-center[

.u-width-70.u-center[
![](images/office-space-done-2-colours.jpg)
]
<br>
.u-no-margin[
### .text-normal[JavaScript 1.0 wurde in]

# 10 Tagen

### .text-normal[geschrieben.]
]
]

.u-margin-top-20.u-background-red.text-white.u-border-radius-10.u-padding-10[
.u-no-margin[
...und vieles davon lässt sich nicht mehr ändern &#9785;
]
]

???
+ stellt sich leider als Fluch der Sprach heraus.
+ zum Vergleich: Clojure wurde über ein Jahr lang entwickelt, viele andere Sprachen machen Versionssprünge im Zuge derer Features abgeschafft werden
+ das geht im Web leider nicht - zu viele Seiten verlassen sich darauf

---

class: s s-bottom s_no-padding s_background-cover
background-image: url(images/p/death-star-2-weakness.jpg)

.s--headline-overlay[
# Verdammt zur Abwärtskompatibilität
]

---

class: s_background-cover

background-image: url(images/death-star-2-boom.gif)

---

class: s s-center s_background-40 s_background-bottom
background-image: url(images/brendan-eich.jpg)

.u-width-70[
.text-quote.text-medium[
„Ich habe 1995 JavaScript verbrochen und versuche es seitdem wiedergutzumachen.“
]
.text-quote--author.text-small[
&ndash; Brendan Eich, JavaScript Jabber Podcast
]
<br><br><br>
]

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

# „Draufspachteln“
.c-list.u-width-70[
+ Semantik von `==` lässt sich nicht mehr ändern, da bestehender Code davon abhängt
+ `===` (strikte Gleichheit) hinzugefügt.

+ Noch gröbere Schnitzer wurden aus der Sprache entfernt: früher ließ sich `undefined` überschreiben.
]  

???
+ `===` schaut sich `typeof` noch an.
+ `NaN === NaN` gibt `false`
+ auf die Variable von `var undefined` wird nicht zugegriffen sondern immer nur auf das echte undefined. `var undefined` wirft keinen Fehler.

---

class: s s-top s_background-bottom s_background-50
background-image: url(images/office-space-lumbergh-hmmm.jpg)

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
// kein Fehler :(
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
background-image: url(images/p/leather-gloves.jpg)

<br>
<br>
# ECMAScript 6 =<br> Lederhandschuhe für JavaScript

???
+ durchkommen der Zacken lässt sich nicht vermeiden (Abwärtskompatibilität), aber man kann jetzt besser an den weniger spitzen Stellen seine Finger ablegen, um das Schwert zu halten

---

background-image: url(images/javascript-logo.jpg)
class: s s-top s_background-20 s_background-bottom

## Warum also JavaScript?

.c-list.u-width-70[
+ nicht bekannt für besondere Eleganz oder Robustheit
  - eher für .text-red[**Brüchigkeit**] und .text-red[**böse Überraschungen**]
  - man _kann_ .text-green[**elegante Programme**] schreiben, aber schwierig
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

class: s_background-cover
background-image: url(images/office-space-lumbergh.jpg)

.u-background-green.text-white.u-width-50.u-padding-20.u-no-margin-vertical.u-border-radius-10[
JavaScript ist trotzdem **super**!
]

???
+ will nicht Freude an JS nehmen oder Euch die Sprache madig machen - ganz im Gegenteil. Trotzdem wichtig, dass man sich anschaut welche Probleme ein Sprachupdate löst - viel zu lernen.
+ lieber als Ruby, obwohl das die sauberere Sprache ist
+ ich schreib gerne JavaScript weil im Browser & allen zeigbar und gut geeignet für funktionale Programmierung / sich hier gerade sehr viel tut mit guten Ideen wie man Frontends bauen kann.
+ normalerweise werden bei Vorträgen zu neuen Sprachversionen nur die Vorteile hervorgehoben und keiner fragt, woran es denn liegt, dass all diese Verbesserungen notwendig waren
+ ES6 ist nicht der Weisheit letzter Schluss, ES7 ist schon in der Mache
+ zeigen warum überhaupt ES6 / Motivation dahinter und Beispiel zeigen wie Programmiersprachen sich über die Zeit entwickeln.
+ zeig euch am Ende noch richtige Handschuhe

---

+ JavaScript war nicht dafür gedacht komplexe Webanwendungen zu schreiben
+ sehr aktives und spannendes Ökosystem

---

"JavaScript is the only language that I’m aware of that people feel they don’t need to learn before they start using it."

---

nicht totzukriegen
https://brendaneich.github.io/ModernWeb.tw-2015/images/alwaysbetonjs.png

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

BEI PRAXISTEIL AM ANFANG SAGEN
# Nicht

+ kein vollständiger Überblick

???
+ ES6 hat zu viele neue Features, als das man sie alle in anderthalb Stunden vorstellen könnte

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

## Tip
nicht fragen welche Sprache oder welches Framework soll ich lernen. Egal was ihr lernt, schaut, dass ihr bessere Programmierer werdet indem ihr Grundlagen lernt, die von Dauer sind :)
JavaScript zu lernen ist gerade eine der sichersten Wetten.

---

Dokumentation:
https://developer.mozilla.org/en/docs/Web/JavaScript

[CologneJS](http://colognejs.de)


Links:
https://brendaneich.github.io/ModernWeb.tw-2015/
https://shaunlebron.github.io/solar-system-of-js

http://exploringjs.com/
https://leanpub.com/understandinges6/read/
https://github.com/addyosmani/es6-equivalents-in-es5
projects.formidablelabs.com/es6-interactive-guide/

https://kangax.github.io/compat-table/es6/

https://github.com/jashkenas/coffeescript/wiki/list-of-languages-that-compile-to-js



---

http://speakingjs.com/es5/ch18.html

Indices are numbers i in the range 0 ≤ i < 232−1.
The maximum length is 232−1.

Indices that are out of range are treated as normal property keys (strings!). They don’t show up as array elements and they don’t influence the property length. For example:

```javascript
var arr = [];

arr[-1] = 'a';
arr       // []
arr['-1'] // 'a'
```

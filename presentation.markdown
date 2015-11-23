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

class: s s-center c-title
background-image: url(images/escher-spiral-cropped.jpg)

.c-title--headline[
# JavaScript und seine Probleme
### und wie ECMAScript 6 helfen kann sie zu lindern
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
+ spannender sich die Motivation und Notwendigkeit hinter ES6 anzuschauen und Euch zu erzählen
+ glaub davon habt ihr langfristig mehr, als wenn wir die neuen Features in aller Tiefe durchgehen
+ könnten eh nicht alle Features besprechen

---

class: s s-center s_background-fit s_background-grey
background-image: url(images/railslove-heart.svg)

.text-white[
# JavaScript
]

???
+ werden heute JavaScripts **Schwächen** anschauen
+ Sprache nicht madig machen
+ trotzdem **eine meiner liebsten Sprachen**, da man nur mit ihr bestimmte spannende Sachen machen kann

---

class: s s-top s_background-grey s_background-50 s_background-bottom
background-image: url(images/paul-kogel.jpg)

## Paul Kögel
.c-list.c-list_narrow[
+ User Interfaces bei [Railslove](http://railslove.com)
+ JavaScript, Ruby und Clojure
+ [@wakkahari](https://twitter.com/wakkahari)
]

???
+ **Ich bin** Paul Kögel
+ Frontends: JavaScript vor allem aus dem **Browser**
+ **freu mich** euch heute ES6 vorzustellen

---

class: s s-top s_background-bottom s_background-30
background-image: url(images/p/dilbert-lunch-cut.png)

# Themen

.row.u-full-width.c-inhalt--list[
.col.col-50.u-padding-left-100[
1. **Hintergrund**
  + Geschichte von JavaScript
  + Probleme von JS/ES5
]

.col.col-50.c-inhalt--ol-with-counter[
2. **ECMAScript 6 Praxis**
  + Neue Sprachfeatures
  + Wie heute schon benutzen?
]
]

???

<!--
3. **Fazit &amp; Ausblick**
  + JS als Assembler des Webs-->

---

class: s s-center s_padding-none s_background-cover
background-image: url(images/p/drawing-board.jpg)

.s--headline-overlay[
# 1. Hintergrund
]

---

background-image: url(images/p/catbert.png)
class: s s-top s_background-bottom s_background-30
<br>
<br>
# <u>Java</u>Script ≠ <u>Java</u>

wie ham-hamster, car-carpet, Hahn-halver Hahn

???
+ eins vorneweg: haben nichts miteinander zu tun

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
+ 1995 von **Brendan Eich** erschaffen, der arbeitete damals bei **Netscape**, die eine Kooperation mit Sun hatten.
+ Mocha &rArr; Marketing: LiveScript &rArr; Marketing: JavaScript
+ **Java** war damals sehr **hip**, Syntax an Java angelehnt, aber Struktur der Sprache ganz anders (**keine Klassen!**)

---

class: s s-top s_background-30 s_background-bottom-with-padding
background-image: url(images/netscape-logo.svg)

## Netscapes Ziel

.c-list[
+ als einfachere Ergänzung zu Java gedacht
+ leicht zugänglich für Amateure
  - interpretiert & untypisiert
  - in HTML einbettbar
]

???
+ leicht zugänglich: kein Kompilierungsschritt, keine Typen, man kann Code aus verschiedenen Quellen zusammenbasteln (copy & paste)

Quellen:
+ JavaScript Jabber withb Brendan Eich
+ http://ghost.jollygoodthemes.com/toffee/the-story-of-javascript

???
.grey[
+ Vorbild: Visual Basic
]

---

class: s s-top s_padding-small

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
    <tr class='text-background-translucent-yellow'>
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
      <td>ES5.1</td>
    </tr>
    <tr class='text-background-translucent-yellow'>
      <td>2015</td>
      <td>"</td>
      <td>"</td>
      <td>ES6</td>
    </tr>
    <tr>
      <td>2016 (?)</td>
      <td>?</td>
      <td>?</td>
      <td>ES7</td>
    </tr>
  </tbody>
</table>

???
+ **Thema Standardisierung** kam recht schnell auf, **browser wars**
+ **ES** = Standard für JavaScript
+ **JS** = Netscape/Mozilla-Implementierung
+ **JScript** = Microsoft
+ **E**uropean **C**omputer **M**anufacturers **A**ssociation, hat auch die CD-ROM standardisiert
+ durften den namen JavaScript nicht benutzen für den Standard
+ erste Version: Juni 1997

.grey[
+ Quellen:  
  -[https://en.wikipedia.org/wiki/JavaScript#Version_history](https://en.wikipedia.org/wiki/JavaScript#Version_history)  
  - [https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence](https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence)  
  - [https://en.wikipedia.org/wiki/ECMAScript#Versions](https://en.wikipedia.org/wiki/ECMAScript#Versions)
]

---

class: s s-top s_background-40 s_background-bottom
background-image: url(images/jagermonkey.jpg)

## JavaScript Engines
+ [Spidermonkey](https://en.wikipedia.org/wiki/SpiderMonkey_%28software%29) (Mozilla)
+ [v8](https://en.wikipedia.org/wiki/V8_%28JavaScript_engine%29) (Chrome, Node.js)
+ [JavaScript Core](https://en.wikipedia.org/wiki/WebKit#JavaScriptCore) ("Nitro", Safari)
+ Chakra (Microsoft)
+ [... mind. 10 weitere](https://en.wikipedia.org/wiki/JavaScript_engine)

???
+ die **Implementierungen** der Dialekte sind JavaScript Engines, VMs in denen JS ausgeführt wird.

.grey[
+ [JS Engines](https://en.wikipedia.org/wiki/JavaScript_engine) sind VMs in denen JS ausgeführt wird.
+ [https://en.wikipedia.org/wiki/JavaScript_engine#The_JavaScript_engine_race:_2008_and_2009](https://en.wikipedia.org/wiki/JavaScript_engine#The_JavaScript_engine_race:_2008_and_2009)
]

---

class: s s-center s_background-20 s_background-bottom
background-image: url(images/p/dogbert.jpg)

#Übersicht

.row[
.col.col-33[
### Sprache
+ .text-green[**JavaScript**]<br>
  .text-mini[(auch Name des Mozilla-Dialekts)]
]

.col.col-33[
### Standard
+ .text-green[**ECMAScript**]
+ TC39 Komitee
]

.col.col-33[
### Versionen
+ ES 5.1
+ .text-green[**ES 6**]<sup>th</sup> Ed. / **ES 2015**
+ ES7

+ "Harmony": alles nach ES5
]
]

???
+ **TC39** (Technical Committee): Gremium mit Vertretern aus der Browserindustrie + geladene Experten

+ für uns **relevante Versionen**
  - ES5.1: in Browsern gerade eingebaut
  - ES6: wird gerade eingebaut
  - ES7: kommt bald

### Standard
+ Version seit 2009, 5.1 (in heutigen Browsern) seit 2011
+ ES6 seit Juni 2015

.grey[
+ [Übersicht der ECMAScript Versionen](https://en.wikipedia.org/wiki/ECMAScript#Versions)
+ [JavaScript - ECMAScript Versionsensprechungen](https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence)
]

---

class: s s-top s_padding-small

## JavaScripts Aufstieg

.u-width-70.text-smaller[
Wandel von Sprache für kleine Spielereien zur Sprache für _Rich Internet Applications_.<br><br>
]

.c-list.c-list_narrow[
+ **1995**: erfunden
+ **1998**: **Mozilla**
+ **2005**: Web 2.0 / **Ajax**
+ **2006**: jQuery
+ **2007**: **iPhone** ohne Flashunterstützung
+ **2008**: **v8** &rArr; viel bessere JS Performanz
+ **2009**: Node.js, ES5
+ **2010**: Backbone.js
+ **2013**: React
]

???
+ 1998 ging **Mozilla** aus Netscape hervor, wichtig für Standardisierung
+ 2005: **Ajax** Revolution
+ 2007: **iPhone**
+ 2008: **v8**
+ ... 2015 - **nächste Folie**

---

class: s s-top s_background-bottom s_background-50
background-image: url(images/full-stack-homer.jpg)

.u-no-margin-bottom[
## JavaScript 2015:
]

+ acht-populärste Programmiersprache
+ allgegenwärtig (Browser, Server, DB, Geräte)
+ Wirtschaft mag _eine_ Sprache für alles


???
+ full stack: Frontend, Backend (nodeJS), Datenbank (Mongo, CouchDB)
+ Roboter, Hardware, etc.

.grey[
+ TIOBE Index vgl.: [http://www.heise.de/developer/meldung/Programmiersprachen-Top-10-Objective-C-raus-Ruby-wieder-rein-2837323.html](http://www.heise.de/developer/meldung/Programmiersprachen-Top-10-Objective-C-raus-Ruby-wieder-rein-2837323.html)
+ [The World's Most Misunderstood Programming Language Has Become the World's Most Popular Programming Language](http://javascript.crockford.com/popular.html)
]

---

class: s s-top s_background-cover s_padding-none
background-image: url(images/p/cat-dog-train.jpg)

.s--headline-overlay[
# Happy choo choo!?? (・_・ヾ
]

???
+ also alles super, wir gehen die neuen Features von ES6 durch und uns haut's alle aus den Socken!?

---

class: s s-center s_padding-none s_background-cover
background-image: url(images/p/grumpy-cat.jpg)

.s--headline-overlay[
# Unangesprochene Probleme
]

???
+ leider nicht, erst müssen wir über JavaScripts Probleme sprechen
+ ** &rArr; Ursprung aller Probleme ist folgender**

+ .grey[Probleme sind wichtiger Teil der Motivation von ES6 und JavaScripts Zukunft sieht gut aus, da es einen regen Austausch über Probleme und riesige Entwicklergemeinde gibt, die in allen Richtungen an Verbesserungsmöglichkeiten arbeitet]

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
+ was erstmal wie ne **stramme Leistung** von Brendan Eich klingen mag...

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

<!--.u-margin-top-20.u-background-red.text-white.u-border-radius-10.u-padding-10[
...und vieles davon lässt sich nicht mehr ändern &#9785;
]
]-->

???
+ ist der **Fluch** der Sprache

---

class: s s-top s_background-40 s_background-bottom
background-image: url(images/brendan-eich.jpg)

.u-width-70[
.text-quote.text-small.c-eich-quote[
„Ich habe 1995 JavaScript **verbrochen** und versuche es seitdem wiedergutzumachen.

[...]
Ich habe einen **Prototypen** gebaut, der zu früh zum ausgelieferten Produkt gemacht wurde und dann konnte ich ihn** nicht mehr ändern**.“
]
.text-quote--author.text-smaller[
&ndash; Brendan Eich
]
]

???
.grey[
+ Quelle: JavaScript Jabber Podcast &amp; Ian Davis Vortrag
]

---

class: s s-bottom s_padding-none s_background-cover
background-image: url(images/p/death-star-2-weakness.jpg)

.s--headline-overlay[
# Verdammt zur Abwärtskompatibilität
]

???
+ kann im Web keine Features zurücknehmen .grey[zu viele verlassen sich darauf]
+ schlechte Teile **werden nicht mehr verschwinden**
+ ES6 fügt nur neue Features hinzu

.grey[
+ zum Vergleich: Clojure wurde über ein Jahr lang entwickelt, viele andere Sprachen machen Versionssprünge im Zuge derer **Features abgeschafft** werden
+ das **geht im Web leider nicht** - zu viele Seiten verlassen sich darauf
]

---

class: s_background-cover
background-image: url(images/death-star-2-boom.gif)

---

class: s s-bottom s_padding-none s_background-cover
background-image: url(images/javascript-good-bad-parts.jpg)

.s--headline-overlay[
# JavaScript in einem Bild
]

???
+ links **"Definitive Guide"**, rechts **"The good Parts"**
+ nur **Teil der Sprache** ist brauchbar

---

class: s s-top s_background-20 s_background-bottom s_padding-small
background-image: url(images/javascript-logo.jpg)

## Warum also JavaScript?

.c-list.u-width-70[
+ nicht bekannt für besondere Eleganz oder Robustheit
  - eher für .text-red[**Brüchigkeit**], .text-red[**böse Überraschungen**], Eigenarten, Widersprüchlichkeiten
  - man _kann_ .text-green[**elegante Programme**] schreiben, aber schwierig
+ .text-green[**Sprache des Webs**]
+ .text-green[**schnell sichtbare Ergebnisse**]
+ .text-green[**allgegenwärtig & universell**]
]

???
+ warum schauen wir uns JS an?

.grey[
+ **Sprache des Webs**: viele Zielgeräte, viele Entwickler
+ **allgegenwärtig**: Browser, Server (Node.js), Datenbanken (Mongo, Couch, ...), Roboter (Nodecopter), Photoshop Plugins, Windows Apps, Native Apps (React Native).
+ **universell**: man kann damit heute fast alles schreiben und die Möglichkeiten wachsen
+ **Full-Stack JavaScript Entwickler**
]

---

class: s s-center

## Sprache im Wandel

.c-list.u-width-70[
+ JavaScript war nicht dafür gedacht **komplexe Webanwendungen** zu schreiben
+ Weiterentwicklung dringend nötig
]

???
.grey[
+ wird heute für _alles_ benutzt
+ sollte möglichst **leichten** Einstieg liefern, Netscape hat sich aber nicht die Zeit genommen die Sprache **einfach** zu halten, sondern früh **Komplexität** angehäuft (z.B. implizite Semikolons)
  - &rArr; Vortrag [Simplicity matters](https://www.youtube.com/watch?v=rI8tNMsozo0) - Rich Hickey
]


---

class: s s-center

## Ziele von ECMAScript 6

.c-list.c-list_narrow.u-width-70[
+ JavaScript besser an heutige Bedürfnisse anpassen
+ **Syntaxerweiterungen** und neue **Features** für besser **verstehbaren** und wartbaren Code
+ **Weiterentwicklung** des Standards dringend nötig, um **Einheit** zu schaffen
+ Verabschiedung dauerte **6 Jahre**, da man Fehler vermeiden wollte, die man dann wieder nicht ausbügeln kann
]

???
+ was uns zu ES6 bringt

.grey[
+ Entwickler wollen Features, die sie aus anderen Sprachen gewohnt sind in JS eingebaut haben
  - **eingebaut**: nicht per Library Modulsystem laden, weil das dann in jedem Projekt anders und miteinander inkompatibel ist
]

---

class: s s-center

## Stand von ECMAScript 6 heute

.c-list.u-width-70[
+ wurde im Juni 2015 verabschiedet
+ **teilweise Unterstützung** in Browsern
+ kann Code nicht ohne **Transpiler** in älteren Browsern nutzen
+ voll **abwärtskompatibel**
  - fügt nur Features hinzu
]

---

class: s s-bottom s_padding-none
background-image: url(images/es6-compatibility.png)

.s--headline-overlay[
# ES6 Kompatibilitätstabelle
]

???
+ wie man an den vielen roten Kästchen sieht gibt es **noch einiges zu tun**
+ .grey[
[https://kangax.github.io/compat-table/es6](https://kangax.github.io/compat-table/es6)
]

---

class: s s-bottom s_padding-none s_background-cover s_background-top
background-image: url(images/p/uk-tap-fixed.jpg)

.s--headline-overlay[
# Probleme von JS/ECMAScript 5
]

???
+ kommen wir zu den **konkreten Problemen** von JS

---

class: s s-center s_background-blue

## I. Drei generelle Probleme von JavaScript<br><br>.text-light-grey.text-medium-small.text-center.u-block[&ndash; Zwischenfazit &ndash;]<br> II. Ein Problem, das ES6 lindern kann

+ gezeigter Code ist ES5, nicht ES6

???
+ generelle Probleme: werden **nicht durch ES6 vollkommen beseitigt**
+ nur _ein_ Beispielproblem für ES6: im ES6 Praxisteil lösen wir mehr

---

class: s s-top s_padding-small

## I.1 Quiz: `Math.max`
```javascript
Math.max()
// ???
```

+ **A**: `Infinity`
+ **B**: `-Infinity`
+ **C**: `9007199254740992`

???
+ bei diesen Quizzes kann man sich **nicht blamieren** - JS ist ziemlich eigenartig

---

class: s s-top s_padding-small

## I.1 Quiz: `Math.max`
```javascript
Math.max()
// ???
```

+ **A**: `Infinity`
+ .text-background-translucent-yellow[**B**: `-Infinity`]
+ **C**: `9007199254740992`

---

class: s s-top s_padding-small s_background-bottom s_background-40 s_padding-small
background-image: url(images/office-space-lumbergh-hmmm.jpg)

## I.1 Quiz: `Math.max` 

```javascript
Math.max();
// -Infinity

Math.min();
// Infinity
```

---

class: s s-top

## I.2 Quiz: Scope

.row[
.col.col-50.u-padding-left-150[
.text-code_medium[
```javascript
var a = 1,
    b = 1;

(function() {
  var a = 2,
      b = 2;
})();

a; // ???
b; // ???
```
]
]

.col.col-50[
.c-list.c-list_narrow[
+ **A**: `a == 1; b == 1;`
+ **B**: `a == 1; b == 2;`
+ **C**: `a == 2; b == 2;`
] 
]
]

???
+ erstmal noch **kein Problem**, Standard JS-Verhalten

---

class: s s-top

## I.2 Quiz: Scope

.row[
.col.col-50.u-padding-left-150[
.text-code_medium[
```javascript
var a = 1,
    b = 1;

(function() {
  var a = 2,
      b = 2;
})();

a; // ???
b; // ???
```
]
]

.col.col-50[
.c-list.c-list_narrow[
+ .text-background-translucent-yellow[**A**: `a == 1; b == 1;`]
+ **B**: `a == 1; b == 2;`
+ **C**: `a == 2; b == 2;`
] 
]
]

???
+ Funktion hat eigenen Scope
+ console.log innerhalb der Funktion würde `2` für `a` und `b` ausgeben

.grey[
+ IIFE muss aufgerufen werden, sonst könnten die äußeren `a` und `b` nicht potentiell überschrieben werden (wenn man in der fn var weglässt werden die äußeren Variablen überschrieben, aber nur wenn man die IIFE aufruft)
]

---

class: s s-top

## I.2 Und wenn man ein Komma vergisst?

.row[
.col.col-50.u-padding-left-150[
.text-code_medium[
```javascript
var a = 1,
    b = 1;

(function() {
* var a = 2
      b = 2;
})();

a; // ???
b; // ???
```
]
]
.col.col-50[
.c-list.c-list_narrow[
+ **A**: `a == 1; b == 1;`
+ **B**: `a == 1; b == 2;`
+ **C**: `a == 2; b == 2;`
]
]
]

---

class: s s-top

## I.2 Und wenn man ein Komma vergisst?

.row[
.col.col-50.u-padding-left-150[
.text-code_medium[
```javascript
var a = 1,
    b = 1;

(function() {
* var a = 2
      b = 2;
})();

a; // ???
b; // ???
```
]
]
.col.col-50[
.c-list.c-list_narrow[
+ **A**: `a == 1; b == 1;`
+ .text-background-translucent-yellow[**B**: `a == 1; b == 2;`]
+ **C**: `a == 2; b == 2;`
]
]
]

---

class: s s-top

## I.2 Antwort: B

.row[
.col.col-50.u-padding-left-150[
.text-code_medium[
```javascript
var a = 1,
    b = 1;

(function() {
* var a = 2
      b = 2;
})();

a; // 1
b; // 2
```
]
]

.col.col-50[
.text-smaller.u-line-height-37[
Der Zeilenumbruch **setzt implizit ein Semikolon**, wodurch<br> `b = ...` keine Variableninitialisierung mehr ist, sondern zur Attributszuweisung auf dem globalen `window`-Objekt wird.
]
]
]

???
.grey[
+ Variableninitialisierungen im globalen Kontext setzen einfach Attribute auf `window`
]

---

class: s s-top

## I.5 `==` (lose Gleichheit)

.row[
.col.col-33[
```javascript
'0' == 0;
// ???
```
]

.col.col-33[
```javascript
0  == '';
// ???
```
]

.col.col-33[
```javascript
'0' == '';
// ???
```
]
]

.c-list.u-width-50[
<br>
+ **A**: `true, true, true`
+ **B**: `true, true, false`
+ **C**: `false, false, false`
]

???
+ Letztes generelles Problem
+ .text-red[direkt zur Lösung 3 Folien weiter springen?]

---

class: s s-top

## I.5 `==` (lose Gleichheit)

.row[
.col.col-33[
```javascript
'0' == 0;
// ???
```
]

.col.col-33[
```javascript
0  == '';
// ???
```
]

.col.col-33[
```javascript
'0' == '';
// ???
```
]
]

.c-list.u-width-50[
<br>
+ **A**: `true, true, true`
+ .text-background-translucent-yellow[**B**: `true, true, false`]
+ **C**: `false, false, false`
]

---

class: s s-top

## I.5 Antwort: B

.row[
.col.col-33[
```javascript
'0' == 0;
// true
```

.text-small[
<br>
_`'0'` wird zu `0` konvertiert._
<br>
]
]

.col.col-33[
```javascript
0  == '';
// true
```

.text-smaller[
<br>
_`''` wird zu `0` konvertiert._
<br><br>
]
]


.col.col-33[
```javascript
'0' == '';
// false
```

.text-smaller[
<br>
_Keine Konvertierung, sind beides schon Strings und einfach nicht gleich._
]
]
]

???
+ Problem von JavaScript, das ES6 nicht löst
+ paradigmatisch für JS Probleme
+ lose Gleichheit: nach Typenkonvertierung
+ **Fazit**: viel nachschauen, um zu verstehen was genau passiert.

.grey[
mittlere Spalte:
```javascript
parseInt('');
// NaN
Number('');
// 0
```

rechte Spalte:
```javascript
'0' === ''
// false
```

Spec: [http://www.ecma-international.org/ecma-262/5.1/#sec-11.9.3](http://www.ecma-international.org/ecma-262/5.1/#sec-11.9.3)
]

---

class: s s-center s_padding-small

## I.3 `==` ist .text-red[**nicht transitiv**]

```javascript
'0' == 0;  // true
 0  == ''; // true
'0' == ''; // false
```

Denn:

```javascript
a == b
b == c
*a != c
```

???
.grey[
+ `==` ist **kommutativ** (Seiten vertauschbar) aber **nicht transitiv** (wenn `a==b` und `b==c` folgt daraus nicht immer, dass auch `a==c`)
+ Erklärung: [http://stackoverflow.com/a/5447170/1881819](http://stackoverflow.com/a/5447170/1881819)

**weitere Beispiele:**
```javascript
undefined == null   // true
false == undefined  // false
false == null       // false

false == '0'        // true

'      ' == 0 // true
'\n\r\t' == 0 // true
```

+ Quellen:
  - http://www.shawnrenner.com/the-dangers-of-double-equals-in-javascript/
  - http://stackoverflow.com/a/359509/1881819
]

---

class: s s-center

## I.3 `==` vs `===`

.c-list.u-width-70[
+ Semantik von `==` **nicht mehr veränderbar** (auch nicht in ES6), da es bestehenden Code kaputtmachen würde
+ Lösung: `===` hinzugefügt (strikte Gleichheit)
+ nie `==` benutzen, nur `===`
+ **JSHint** warnt vor Verwendung von `==`
]

???
+ **strikte Gleichheit**: prüft Typen mit (`typeof`)
+ Brendan Eich wollte für JavaScript 1.2 einen Opt-in einbauen, verworfen, da es zu wenig Leute benutzt hätten

---

class: s s-center s_padding-none s_background-cover
background-image: url(images/p/office-space-the-bobs.jpg)

.s--headline-overlay[
# Zwischenfazit
]

---

class: s s-center

## Zusammengefasst ..

.c-list.u-width-70[
+ überraschende Voreinstellungen (`Math.max`)
<!--+ Arrays sind numerisch _und_ assoziativ indiziert -->
+ implizite Semikolons
+ JS hat ungewohnten Funktionsscope
+ `==` ist gefährlich
+ mehr: [wtfjs.com](http://wtfjs.com)
]

???
.grey[
+ ... wir haben nur eine Stichprobe der Probleme gesehen
]

---

class: s s-center

## ES6 zur Hülf!

.c-list.c-list_narrow.u-width-70[
+ **_Ursachen_ nicht durch ES6 lösbar**, aber ES6 fügt neue Möglichkeiten hinzu Probleme **zu umgehen**
+ Codeanalysetools wie **JSHint** sind hilfreich
]

???
.grey[
+ JSHint: wenn man's denn benutzt
+ _Principle of Least Surprise_ verletzt
 - relativ viele versteckte Fehlerquellen
+ JS ist schwer, Erfahrung wichtig
]

---

class: s s-top

# Wenn JavaScript eine Waffe wäre...

![If JavaScript were a weapon: sword without a hilt](images/javascript-weapon.png)

.text-center.text-mini[
Quelle: [If programming languages were weapons](http://bjorn.tipling.com/if-programming-languages-were-weapons)
]

???
+ **Schwert ohne Griff**, bei dem man sich unweigerlich blutige Finger holt

---

class: s s-top s_background-bottom
background-image: url(images/p/leather-gloves.jpg)

.u-no-margin-vertical[
## ECMAScript 6 =<br> <u>Leder</u>handschuhe für JavaScript
]
.u-width-70.text-small[
+ .text-smaller[man kann sich immer noch verletzen]
+ .text-smaller[man muss die Handschuhe nicht anziehen (kann immer noch ES5 schreiben)]
+ .text-smaller[_wenn_ man sie anzieht (d.h. neue ES6-Funktionen nutzt), wird das Arbeiten mit JavaScript um einiges angenehmer]
]

---

class: s s-top s-left
## II. <u>Implizite globale Variablen</u> &amp; Hoisting

```javascript
var foo = "Ich bin global";

(function() {
  var foo = "Ich bin lokal";
})();

foo; // "Ich bin global"
```

???
+ Problem das **ES6 adressiert**
+ Codebeispiele sind immer noch ES5, nicht 6
+ hatten es bei den Scopes gerade ja schon, **wenn ich jetzt `var` weglasse**...

---

class: s s-top s-left
## II. <u>Implizite globale Variablen</u> &amp; Hoisting

```javascript
var foo = "Ich bin global";

(function() {
* foo = "Ich bin lokal";
})();

*foo; // "Ich bin lokal"
```

???
+ wenn ich jetzt `var` in der Funktion vergesse, verändere ich auf einmal das globale `foo`. 

.grey[
+ wenn es `foo` global noch nicht gäbe würde JS mir mal eben eine machen (aber nicht im **strict** mode)
+ JS macht hier **zu viele Annahmen** darüber was ich machen will
]

---

class: s s-top s-left
## II. Implizite globale Variablen &amp; <u>Hoisting</u>

```javascript
var foo = "Ich bin global";

(function() {
* console.log(foo); // ???
  foo = "Ich verändere das globale foo!?";
  // ...
* var foo = "Ich bin lokal";
})();

*foo; // ???
```

???
+ Nun zum sog. **Hoisting** (Flaggenhissen)
+ Was passiert mit dem globalen `foo`, wenn wir **am Ende** der Funktion eine lokale Variable `foo` initialisieren?
+ Und was gibt console.log am Anfang der Funktion aus?

---

class: s s-top s-left
## II. Implizite globale Variablen &amp; <u>Hoisting</u>

```javascript
var foo = "Ich bin global";

(function() {
* console.log(foo); // undefined
  foo = "Ich verändere das globale foo!?";
  // ...
* var foo = "Ich bin lokal";
})();

*foo; // "Ich bin global"
```

???
+ Hoisting: **Variablen*deklaration* (aber nicht -initialisierung) steigy zum Anfang der Funktion auf**.
+ Woher weiß ich beim ersten `foo = `, dass unten noch `var` kommt? Was, wenn das jemand später hinzufügt?

---

class: s s-top s_background-bottom s_background-40
background-image: url(images/flag.png)

# Hoisting

.c-list.u-width-70[
+ **gefährlich**
+ manchen Texte erwecken den Eindruck als sei es sinnvolles Sprachfeature, das es zu beherrschen gelte
+ ES6 Gegenmittel: `let` statt `var` benutzen
]

---

class: s s-center s_background-green s_padding-none

.s--headline-overlay[
# 2. ECMAScript 6 Praxis
]
.unstyled-wrapper[<br>
## A. Sprachfeatures<br><br>B. Wie heute schon benutzen?
]

???
+ kein vollständiger Überblick

---

class: s s-top

# `let` - Variablen mit Blockscope

.row[
.col.col-50.u-no-padding-horizontal[
.text-code_medium[
```
var outer = true;
if(true) {
*  var inner = outer;
}
*console.log(inner === outer);
// true
```]
]

.col.col-50.u-no-padding-horizontal[
.text-code_medium[```
let outer = true;
if(true) {
*  let inner = outer;
}
*console.log(inner === outer);
// ReferenceError:
// inner is not defined
```]
]
]

---

class: s s-top

# `const` - Konstanten mit Blockscope

```javascript
const A_CONSTANT = 'Hello, hello!';

A_CONSTANT = ''; // Fehler "A_CONSTANT" is read-only"
```

---

## Template Strings zur Interpolation

```javascript
let user = {first: 'Peter', last: 'Parker'};

// ES5
var fullName = user.first + ' ' + user.last;
// 'Peter Parker'

// ES6
*let fullName = `${user.first} ${user.last}`
// 'Peter Parker'
```

---

class: s s-top

## Pfeilfunktionen

```javascript
let user = {first: 'Peter', last: 'Parker'};

*let fullName = (first, last) => {
  return `${first} ${last}`;
}

fullName(user.first, user.last);
// 'Peter Parker'

// ES5
var fullName = function(first, last) {
  // ...
};

```

---

class: s s-top

## Pfeilfunktionen auf Objekten
.u-no-margin-vertical[
`this` ist automatisch richtig gesetzt!
]

.text-code_medium[
```
// ES6
let car = {
   model: 'Mercedes-Benz',
   drivers: ['Anna', 'Bob'],
   logDrivers() {
      this.drivers.forEach((driver) => {
*       console.log(`${driver} drives ${this.model}`)
      });
   }
};
```
]

???
+ in ES5 müsste `this` vorher in `self` oder `that` gespeichert werden.

---

# Klassen

```javascript
class Vehicle {
  constructor(name) {
    this.name = name;
    this.kind = 'vehicle';
  }
  getName() {
    return this.name;
  }
}

let myVehicle = new Vehicle('rocky');
```

---

# Vererbung

```javascript
class Car extends Vehicle {
  constructor(name) {
     super(name);
     this.kind = 'car'
  }
}
```

---

# Module: `export`

```javascript
// lib/math.js
*export function sum(x, y) {
  return x + y;
}
*export var pi = 3.141593;


// app.js
import { sum, pi } from "lib/math";
```

???
+ mehrere `export`s in einer Datei
+ `export` muss explizit sagen was exportiert wird (function oder var)

---

# Module: `export default`

```javascript
// lib/do-something.js
*export default function() {
  return 1;
}


// app.js
*import doSomething from 'lib/do-something';
doSomething();
```

---

class: s s-top

## Destrukturierung von Objekten

```javascript
let user = { first: "Peter", last: "Parker"};

*let {first, last} = user; // Reihenfolge egal
first; // "Peter"


*let {first: f, last: l} = user; // mit Aliasen
f; // "Peter"
```

---

## Destrukturierung von Funktionsargumenten

```javascript
let user = {first: 'Peter', last: 'Parker'};

*let greet = ({first, last}) => {
  return `Hallo, ${first} ${last}!`;
}

greet(user); // 'Hallo, Peter Parker!'
```

---

# Destrukturierung von Arrays

.text-code_medium[
```javascript
// ES5
var first = someArray[0];
var second = someArray[1];
var third = someArray[2];

// ES6
*let [first, second, third] = someArray;

*let [first, second, ...rest] = [1, 2, 3, 4, 5];
first;     // 1
second;    // 2
rest;      // [3, 4, 5]
```
]

+ `...` heißt **Spreadoperator**

---

# Destrukturierung von Arrays

```javascript
*let [x, y] = ['a']
x; // 'a'
y; // undefined
```

### Mit Standardwerten

```javascript
*let [x, y='b'] = ['a']
x // 'a'
y // 'b'
```

---

# Standardwerte bei Funktionen

```javascript
*function doSomething(a, b = 0) {
  return([a, b]);
}

doSomething(2);
// [2, 0]
```

---

# Objektliterale in Kurzschreibweise

```javascript
let name =  'Jim Smith';
let email = 'jim@smith.com';
*let user = { name, email };

user // {name: 'Jim Smith', email: 'jim@smith.com'}
```

Kurzschreibweise für:
```javascript
let user = { name: name, email: email }
```

---

class: s s-center

# Neue Arraymethoden

```javascript

[5, 1, 10, 8].find(n => n === 10) // 10

[5, 1, 10, 8].findIndex(n => n === 10) // 2
```

???
+ man kann Pfeilfunktionen auch in einer Zeile schreiben

---

class: s s-center

# Spreadoperator

statt `apply`:
```javascript
let attributes = ['Peter Parker', 'peter@parker.com']

let buildUser = (name, email) => {
  return { name, email };
}

*buildUser(...attributes);
// { name: "Peter Parker", email: "peter@parker.com" }
```

---

class: s s-center

# Zugewinne durch ES6

.c-list.u-width-70[
+ Syntaxverbesserungen
+ .text-background-translucent-yellow[ `this` in Pfeilfunktionen]
+ .text-background-translucent-yellow[block scope durch `let`
]
+ wichtige Vereinheitlichungen durch Einbetten in Sprache von:
  - **Klassen**
  - **Modulen**
]

---

class: s s-center

# Einige weitere ES6 Features
+ Promises
+ Generator-Funktionen
+ Symbols
+ Maps
+ Sets
+ Erweiterungen der Standardbibliothek

???
.grey[
+ Maps: An Object has a prototype, so there are default keys in the map. This could be bypassed by using map = Object.create(null) since ES5, but was seldomly done.
The keys of an Object are Strings and Symbols, where they can be any value for a Map.
[https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map)
]

---

class: s s-center s_background-blue

# B. Wie heute schon benutzen?

---

class: s s-top s_background-35 s_background-bottom
background-image: url(images/babel.png)

.u-margin-bottom-20[
# ES6 heute nutzen
]

.c-list.u-width-70[
+ [**Babel**](https://babeljs.io/): transpiliert ES6/7 zu ES5
+ daneben **Webpack** / Browserify als Packaging Tools, um ES6 Module zu nutzen
+ [paulkogel/simple-babel-webpack-starter-pack](https://github.com/paulkogel/simple-babel-webpack-starter-pack)
]

???
+ Link zu Jeremy Ashkenas-Vortrag "The Transpilers are coming"

---

class: s s-center s_background-blue

# ENDE. Fragen?

Danke für's Zuhören.  
Lasst mich wissen, wenn ihr was gebaut habt oder Probleme habt.

@wakkahari  
paul@railslove.com

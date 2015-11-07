class: s-vertical-center s-center c-title
background-image: url(images/escher-spiral-cropped.jpg)

.c-title--headline[
# ECMAScript 6
### die neueste Version von JavaScript
]

.c-title--meta[
.c-title--author[
  Paul Kögel
]
.c-title--links[
  [@wakkahari](https://twitter.com/wakkahari) &ndash; <paul@railslove.com>
]
]

.c-title--note[
  'p' drücken, um Präsentationsnotizen ein-/auszublenden]

---

class: s-vertical-center s_background-grey
background-image: url(images/paul_kogel_wakkahari.jpg)

.full-page-link[
[](https://twitter.com/wakkahari)
]

???
+ Entwickler bei **Railslove**: Webfrontends mit JavaScript, Ruby und Clojure

---

class: s-vertical-center

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

class: s-vertical-center s_no-padding s_background-grey c-garden-bosch
background-image: url(images/hieronymus-bosch-the-garden-of-earthly-delights-crop.jpg)

.s--headline-overlay[
# 1. Orientierung
]

???
Dschungel von Namen, ständig neue Entwicklungen

---

class: s-vertical-center

# <u>Java</u>Script ≠ <u>Java</u>

???
+ fangen wir von ganz außen an
+ das Wichtigste, was man über JavaScript wissen muss

---

class: s-vertical-center

# JavaScript: 1995-...

.row[
.col.col-33[
### Brendan Eich
![Brendan Eich](images/brendan-eich.jpg)
.text-tiny.text-grey-inherit[
<br><br>
source: Darcy Padilla  
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

class: s-vertical-center

## Die wesentlichen Teile<br> von JavaScript wurden in
# .text-red[10 Tagen]
## geschrieben.

---

class: s-vertical-center

.text-quote.text-medium[
“I perpetrated JavaScript ...”
]
.text-quote--author.text-small[
\- Brendan Eich, JavaScript Jabber Podcast
]

---

class: s-vertical-center

# Duale Natur
.u-width-70[
![](images/javascript-good-bad-parts.jpg)
]

???
im linken Buch steht alles über JavaScript
das rechte Buch bekommt man, wenn man die ganzen Sachen, die an JavaScript schlecht sind, aus dem dicken Buch herausreißt.

---

background-image: url(images/eminem-c-hammer.jpg)

???
+ passendste Metapher - gerade im Hinblick auf ES6: Man hat Eminem und der kann nicht gut genug rappen. Dann fängt man an MC Hammer drüberzukleistern und es sieht immer mehr wie n richtiger Rapper aus, aber immer wieder scheint dieser Eminem durch.

ES6: großer Schritt n anständiger Rapper, eine solide Programmiersprache zu werden - nichts gegen Eminem.

---



# Heute
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

class: s-vertical-center

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
+ durften den namen JavaScript nicht benutzen für den Standard
+ erste Version: Juni 1997
+ Version seit 2009, 5.1 (in heutigen Browsern) seit 2011
+ ES6 seit Juni 2015

+ [Übersicht der ECMAScript Versionen](https://en.wikipedia.org/wiki/ECMAScript#Versions)
+ [JavaScript - ECMAScript Versionsensprechungen](https://en.wikipedia.org/wiki/ECMAScript#Version_correspondence)

---

class: s-vertical-center

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


---

Dokumentation:
https://developer.mozilla.org/en/docs/Web/JavaScript

[CologneJS](http://colognejs.de)


Links:
https://brendaneich.github.io/ModernWeb.tw-2015/
https://shaunlebron.github.io/solar-system-of-js

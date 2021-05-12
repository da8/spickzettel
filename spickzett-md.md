# Absätze und Umbrüche  

Absätze werden durch
Leerzeilen voneinander
getrennt.


Einen Umbruch erzwingt man
durch zwei Leerzeichen
vor  
dem Umbruch. Einfache
Umbrüche
werden ignoriert.

# Überschriften
# Überschrift 1. Grades
## Überschrift 2. Grades ##
...
###### Überschrift 6. Grades
Überschrift 1. Grades
=====================
Überschrift 2. Grades
---------------------
Optional kann man Überschriften mit entsprechenden #-Symbolen abschließen

# Listen und Aufzählungen
* Ungeordnete Listen beginnen
mit einem *, - oder +.
* Verschachtelung durch
  * Einrückung mit mindestens
    zwei Leerzeichen oder
    einem Tab.
  * Absätze entstehen
    durch Fortsetzung  
    der Einrückung
1. Aufzählungen beginnen
   mit Zahlen
9. Die richtige Nummerierung
5. ist nicht wichtig

# Hyperlinks
[Link-Text](http://url.tld)  
[Link](http://url.tld "title")  

Referenzierte Links:
[Link-Text][id]  
Link auf [Mac & i].  
[Link][id2] mit Title-Attribut  

[id]: http://url.tld
[Mac & i]: http://mac-and-i.de
[id2]: http://url.tld "title"

# E-Mail-Adressen und URLs
Verlinkte <mail@adresse.tld>  
Verlinkte URL <http://url.tld>  

# Bilder
![Alt-Text](pfad/bild.png)  
Referenzierte Bilder: Ein Bild ![Alt-Text][id]  
[id]: pfad/bild.png  

# Zitate (Blockquotes)
> Zitat-Blöcke funktionieren  
> wie bei E-Mails
> > inklusive Verschachtelung

# Code-Blöcke
Code-Blöcke

    mit vier *Leerzeichen*
    oder einem **Tab**
    [einrücken][].

Inline-'**[Code][]**'

# Trennlinie
---
***
Mindestens drei alleinstehende _, * oder - mit oder ohne Zwischenraum.

# Escape-Sequenz

3\. Keine Aufzählung  
Text mit \*Sternchen\*

Die Escape-Sequenz gilt für: \, `, *, _, {, }, [, ], (, ), #, +, -, ., !  

# Fußnoten
Text mit Fußnote[^fussnote]  
... Beliebiger Text ...  
[^fussnote]: Fußnoten-Text  

# Tabellen

| Spalte 1 | Spalte 2 | Spalte 3 |
| :------- | :------: | -------: |
| Zeile 1 | Verbundene Zelle ||
| Links | *Mitte* | Rechts |

# Meta-Daten

Title:    MultiMarkdown-CheatSheet  
Date:    2014-01-28  
Author:    Mark Down, Mac Andi    
Keywords: PDF, Spickzettel, Deutsch  

Meta-Daten stehen am Anfang der Datei und werden mit einer Leerzeile vom Text getrennt. Doppelte Leerzeichen am Zeilenende erhöhen die Lesbarkeit in Programmen, die beispielsweise nur Standard-Markdown verwenden.

# Ressources
* [Markdown](https://daringfireball.net/projects/markdown/)
* [MultiMarkdown](http://fletcherpenney.net/multimarkdown)
* [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#lists)
* [Markdown Cheat Sheet - Heise](https://www.heise.de/mac-and-i/downloads/65/1/1/6/7/1/0/3/Markdown-CheatSheet-Deutsch.pdf)

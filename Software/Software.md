# Einordnung von Programmiersprachen
- Java/C#
  - Für Alles
  - Objektorientiert 
  - Wir in Bytecode vorcompiliert
    - Wird während der Laufzeit Interpretiert
    - Läuft auf jeden Betriebssystem, das eine kompatible Runtime environment (Laufzeitumgebung) hat
- JavaScript
  - Für das Internet
  - Läuft im Browser
  - Meist Client-seitig 
- PHP
  - Für das Internet
  - Läuft Server-seitig
- CSS
  - Styling für HTML-Seiten
  - Stylesheet
- HTML
  - Für das Internet 
  - Markup Language
- XML
  - Für Infromationen 
    - zb. Konfiguration
  - Post HTTP-Requests 
- Bash
  - Linux Terminal
  - Skripte
- Assembler
  - Maschinen-nahe Programmierung
    - Gerätetreiber
    - Zeitkritisches 
- C
  - Maschinen-nahe Programmierung
    - Nicht so nah wie Assembler
    - Gerätetreiber
    - Microcontroller
    - Betriebsysteme 
    - Programmiersprachen
# Debugging (Fehlersuche)
- Überwachen von Variablen während der Laufzeit.  
- Loggen von Errormessages mit Stack Trace.  
- Breakpoints setzen.
- Schrittweises Durchlaufen des Codes.
- Isolieren verschiedener Funktionalitäten und unabhängiges Testing.
- Unit Tests.

# Refactoring 
Umgestaltung/ "Aufräumen" eines bereits funktionalen (meist veralteten) Codes nach folgenden Punkten:

- Lesbarkeit
- Übersichtlichkeit
- Verständlichkeit
- Erweiterbarkeit
- Vermeidung von Redundanz
- Testbarkeit
- Änderungen am Programmierstil bzw. den Coding Conventions

Möglichkeiten: Auslagern, Zusammenfassen ähnlicher Funktionen, Beseitigen von totem Code, Umbenennen von Variablen, Methoden, Objekten, usw...
# Algorithmus
Von Wikipedia (passt schon so)

## Definition 
Eine Berechnungsvorschrift zur Lösung eines Problems heißt genau dann Algorithmus, wenn eine zu dieser Berechnungsvorschrift äquivalente Turingmaschine existiert, die für jede Eingabe, die eine Lösung besitzt, stoppt.

## Eigenschaften des Algorithmus
Aus dieser Definition sind folgende Eigenschaften eines Algorithmus ableitbar:

- Das Verfahren muss in einem endlichen Text eindeutig beschreibbar sein (Finitheit).
- Jeder Schritt des Verfahrens muss tatsächlich ausführbar sein (Ausführbarkeit).
- Das Verfahren darf zu jedem Zeitpunkt nur endlich viel Speicherplatz benötigen (Dynamische Finitheit).
- Das Verfahren darf nur endlich viele Schritte benötigen (Terminierung).

Darüber hinaus wird der Begriff Algorithmus in praktischen Bereichen oft auf die folgenden Eigenschaften eingeschränkt:

- Der Algorithmus muss bei denselben Voraussetzungen das gleiche Ergebnis liefern (Determiniertheit).
- Die nächste anzuwendende Regel im Verfahren ist zu jedem Zeitpunkt eindeutig definiert (Determinismus).
# HTML und XML
HTML und XML sind beides Tag-basierte Auszeichnungssprachen (Markup Language), die sich, abgesehen von der Verwendng und den verwendeten Tags, nur wenig unterscheiden.  

## Aufbau
### Deklaration
Bei beiden Sprachen kommt als erstes eine Art Überschrifft, die als Sprachdeklaration gilt.  
Für __XML__ lautet diese zb.:  
```XML
<?xml version="1.0" encoding="UTF-16"?>
```
Hier wird angegeben, dass es sich um XML in der Version '1.0' handelt. Zusätzlich wird hier auch das optionale `encoding`-Tag angegeben. 

Dies sieht für __HTML__ ähnlich, aber nicht gleich aus: 
```HTML
<!DOCTYPE html>
```
Hier wird lediglich angegeben, dass es sich um HTML handelt.  
Früher wurde hier auch die HTML-Version angegeben. Das ist nicht mehr notwendig.

### Content
Nach der Deklaration folgen nun bei beiden Sprachen der eigentliche Inhalt.  

__XML__ ist im Allgemeinen sehr frei in seiner Struktur. Bis auf, dass sich Tags nicht überschneiden dürfen und jeder Tag in der Regel auch geschlossen werden muss, ist das Stukturieren der XML-Struktur gänzlich uns überlassen.  
Durch diese Sprachstruktur lassen sich Datenstrukturen, wie zb. Listen und genestete Objekte abbildnen. 
__Beispiel XML__:  
```XML
<?xml version="1.0" encoding="UTF-16"?>
<content>
    <user>
        <name>Peter</name>
        <accounts>
        	<value>
                <name>xX_PeternatorHDLP_Xx</name>
            </value>
            <value>
                <name>Schlepphodn420</name>
            </value>
        </accounts>
    </user>
</content>
```
> Wir können die Struktur auch mit Pfaden zu bestimmten Objekten ausdrücken.  
> zb.:  
> `content.user.name` 
> oder
> `content.user.acounts[0].name`

__HTML__ hat, im gegensatz zu XML, eine recht strickte Struktur, die darauf abziehlt das Document Object Model (DOM) abzubilden.  

__Beispiel HTML__
```HTML
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"/>
        <title>Seitentitel</title>
    </head>
    <body>
        <h1>Überschrifft</h1>
        <p>Text</p>
    </body>
</html>
```
Wichtige Tags sind zb.:
- p 
  - Text Paragrafen
- b 
  - Fett druck (Bold)
- i
  - Schiefdruck (Italic)
- u
  - Unterstrichen 
- h1 - h6
  - Überschriften
- span 
  - Leeres Element
- div
  - 'container'
- button
- input
  - bsp. type="text" usw.
- form
> Sehe https://www.w3schools.com/

# Pseudo-Code
Bei Pseudo-Code gelten nicht allzu viele Regeln. Er sollte aber einem konsequenten Syntax folgen, etablierte Kontrollstrukturen, also Anweisungen wie `if` oder `switch` und Schleifen wie `for` oder `while`, können/sollten genutzt werden und es sollten nicht zu viele Aspekte des eigentlichen Implementierens in fake-funktionen abstrahiert werden.  

Im Allgemeinen können aber systemabhängige Funktionen des Betriebsystem immer abstahiert werden. So können wir zb. zur Ausgabe von Daten eine Methode namens print() oder vlt auch ausgabe() benutzen. Solange die Funktion selbsterklärend benannt ist, können wir hier kreativ sein.  

Der Code kann sich an der Syntax verschiedenster Sprachen orientierten, aber da der Code nachher handschrifftlich vorliegen wird, empfehle ich eine C-Orienierte Syntax, mit Klammern, zu verwenden, wie es zb. Java, JavaSkript oder C# machen. 

__Beispiel__:
```Scala
main(args: string[]) {
    if (args.size() <= 0) {
        erorr("Missing Arguments!")
    } 
    switch (args[0]) {
        case 'a': 
            print("AAA!!!")
            break
        default:
            print("Illegel Argument!")
    }
}
```
# Struktogramme und UML
Siehe Formelsammlung, die ich in Discord geschickt hab'.  
Raum #dateien

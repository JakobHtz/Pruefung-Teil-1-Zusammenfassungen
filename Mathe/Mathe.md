# Einheitentabelle zur Umrechnung 
Bezeichnung | Präfix | Wert 
--- | --- | --- 
kilo | k | $10^{3}=1.000$
mega | M | $10^{6}=1.000.000$
giga | G | $10^{9}=1.000.000.000$
tera | T | $10^{12}$
peta | P | $10^{15}$
exa | E | $10^{18}$
zetta | Z | $10^{21}$
yotta | Y | $10^{24}$

Bezeichnung | Präfix | Wert 
--- | --- | --- 
kibi | ki | $2^{10}=1.024$
mebi | Mi | $2^{20}=1.048.576$
gibi | Gi | $2^{30}=1.074.741.824$
tebi | Ti | $2^{40}$
pebi | Pi | $2^{50}$
exbi | Ei | $2^{60}$
zebi | Zi | $2^{70}$
yobi | Yi | $2^{80}$

# Zahlensysteme 
Die von uns verwendeten Zahlensysteme (Hex., Dez., Dual) sind alles Stellenwertssysteme. Das heißt, dass eine Ziffern je nach ihrer Stellung innerhalb der Zahl eine andere Wertigkeit hat.

So sind zb. 01 und 10 Zahlen von komplett verschiedener Wertigkeit.  
Obwohl sie die gleichen Ziffern enthalten, haben diese in deren jeweiligen Kontext verschiedene Werte. 

Diese Wertigkeit ist zudem auch innerhalb verschiedener Basen zumeist unterschiedlich.

Die Wertigkeit in Dezimal, abhängig von Stellung und Basis, können wir folglich berrechnen:

$\sum_{i=0}^{n}{b^{i}}z_i$

> Hier bei gilt:  
> - Die Zahl wird von Rechts nach Links gelesen.  
> - $i$ ist der Index beginnend mit 0.
> - $n$ ist die Länge der Zahl - 1.
> - $b$ ist die Basis.  
> - $z_i$ ist die Ziffer an Stelle '$i$'.

__Beispiel__:  
Errechnen der Wertigkeit von $42_{16}$.  
$\ \ \ \ 16^{0}*2 = 2$  
$+\ 16^{1}*4 = 64$  
$= 66$

## Dual 
Basis 2, bzw. Dual besitzt nur 2 Ziffern. 
- 0
- 1

Somit ist Dual ein sehr simples System, dass deswegen auch zb auf Computern Verwenung findet.

__Beispiel__:  
$11010001_2 = 209_{10}$

## Hex 
Basis 16, bzw. Hexadezimal, bzw Hex. besitzt 16 Ziffern.  
Dies sind die Zahlen 0-9 + Buchstaben A-F, welche stellvertretend für die Zahlenwerte 10-15 stehen. 

Die einfache Umrechenbarkeit zwischen Binär und Hexadezimal hat es zu einem häufig verwendeten Zahlensystem in der Informatik werden lassen.

So können Binärzahlen spielend ohne irgendeine Rechnung umgeschrieben werden.  

__Beispiel__:  
$11010001_2 = D1_{16} = 209_{10}$  
Dabei wird die Dualzahl von Links nach Rechts in Vierergrüppchen aufgeteilt (zb. 1101.0001) und diese Vierergrüppchen einzeln umgerechnet (also $1101_2 = D_{16}$ und $0001_2 -> 1_{16}$).  
Dies Funktioniert da die Basen Potenzen von einander sind.  
Beides sind Zweierpotenzen.  
> Das funktioniert auch mit Oktal (der Basis 8) und Dreiergrüppchen von Binärzahlen. Die Begründung bleibt die Selbe.

## Dezimal 
Das Zehnersystem kennt jeder du H0nd.

__Beispiel__:  
$69_{10} = 69$

# Umrechnung
## Divisionsverfahren
Wollen wir eine Dezimalzahl in eine bestimmte Basis umrechnen, so können wir wiederholt durch diese Basis Teilen, den Rest notieren und daraus die gewünschte Zahl zusammen setzen. 

__Beispiel__:  

$234_{10} = ?_2$  
$234:2=117\ Rest\ 0$  
$117:2=58\ Rest\ 1$  
$58:2=29\ Rest\ 0$  
$29:2=14\ Rest\ 1$  
$14:2=7\ Rest\ 0$  
$7:2=3\ Rest\ 1$  
$3:2=1\ Rest\ 1$  
$1:2=0\ Rest\ 1$  
$0:2=0\ Rest\ 0$  
$0:2=0\ Rest\ 0$  

Wollen wir die Zahl jetzt in Schreibrichtung (Links nach Rechts) zusammensetzen, schreiben wir die Reste von der letzten Signifikanten Stelle von Unten nach Oben auf.  
$=11101010_2$  
> Wenn du vergisst in welche Richtung du die Zahl aufschreiben musst, denke daran, dass du durch diese Rechnung unendlich viele Nullen an die Zahl anhängen müsstest, wenn du nicht abbrichst.   
> Dies geht nur in eine Richtung ohne den Wert der Zahl zu verändern!!!  
> Also ist es $0..00011101010$ und __auf gar keinen Fall__ $01010111000..0$!!!  
> So ergibt sich die Richtung also logisch.

## Subtraktionsverfahren
Wenn wir eine Bezimalzahl in eine bestimmte Basis überführen wollen, können wir aber auch das Subtraktionsverfahren nutzen.  
Beim Subtraktionsverfahren ziehen wir jeweils die größt mögliche Potenz der gewählten Basis ab, die uns nicht ins negative bringt.  
Wir notieren den Exponenten, um so die Stellen herauszufinden an denen in der Binär darstellung eine 1 stehen wird.  

Wie schon erwähnt geht dies auch mit anderen Basen, aber dies wird um einiges aufwendiger, warum ich es hier mal ignoriere.

### Allgemeine Formel
$\sum_{i=n}^{0}{Zahl_{10} - b^{i}*z_i}$

### Formel für Binär Zahlen
$\sum_{i=n}^{0}{Zahl_{10} - 2^{i}}$

__Beispiel__:  

$234_{10}-2^{7}=234_{10}-128$ &#10003;  
$106_{10}-2^{6}=234_{10}-64$ &#10003;  
$42_{10}-2^{5}=234_{10}-32$ &#10003;  
$10_{10}-2^{4}=234_{10}-16$ &#10007;  
$10_{10}-2^{3}=234_{10}-8$ &#10003;  
$2_{10}-2^{2}=234_{10}-4$ &#10007;  
$2_{10}-2^{1}=234_{10}-2$ &#10003;  
$0_{10}-2^{0}=234_{10}-1$ &#10007;  

$=11101010_2$
> Denk bei der Richtung an die Stellenwerte. 

## BiBi-Formel
Durch die BiBi-Formel können wir, wie oben schon beschrieben, die Wertigkeit aller Ziffern in Dezimal umwandeln.

$\sum_{i=0}^{n}{b^{i}z_{i}}$

__Beispiel__:  

$11101010_2$ 

$\ \ \ \ 0*2^{0} = 0$  
$+\ 1*2^{1} = 2$  
$+\ 0*2^{2} = 0$  
$+\ 1*2^{3} = 8$  
$+\ 0*2^{4} = 0$  
$+\ 1*2^{5} = 32$  
$+\ 1*2^{6} = 64$  
$+\ 1*2^{7} = 128$  
$=234$  

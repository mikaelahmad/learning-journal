# KI Version
# Crash Course CS — Folge 3 + 4

> **Wichtige Folgen:** Boolean Logic + Binary Representation sind das konzeptionelle Bindeglied zwischen Hardware (Transistoren) und Software (Logik, Daten). Wer das versteht, versteht im Kern, wie aus Strom "Computer" wird.

## Folge 3: Boolean Logic & Logic Gates

### Kernideen
- Computer arbeiten mit nur **zwei Zuständen** (1/0, true/false) — das ist die Brücke zwischen Physik (Strom an/aus) und Logik
- Aus den vier Logic Gates **AND, OR, NOT, XOR** lässt sich **jede beliebige Rechenoperation** bauen (Addieren, Vergleichen, Speichern) — das ist die Grundlage aller modernen CPUs
- **Transistoren** sind die physikalische Umsetzung dieser Logic Gates: ein Schalter, der Strom durchlässt oder blockiert

### Konzepte / Begriffe, die neu für mich waren
- **Bit** — kleinste Informationseinheit, repräsentiert *true* (Strom fließt) oder *false* (kein Strom)
- **Ternary / Quinary Systeme** — alternative Systeme mit 3 bzw. 5 Zuständen (theoretisch möglich, in Praxis kaum genutzt — binär ist robuster und einfacher zu implementieren)
- **Boolean Algebra** — Mathematik mit Wahrheitswerten statt Zahlen; Variablen sind true/false, Operationen sind logisch
- **Transistor-Aufbau** — hat einen Steuerdraht (Control Wire) als Input und zwei Elektroden; je nach Steuerdraht-Signal fließt Strom oder nicht
- **Logic Gate** — physikalische Schaltung aus Transistoren, die eine Boolean-Operation umsetzt
- **NOT** — invertiert den Eingangswert: true → false, false → true
- **AND** — true nur, wenn beide Eingänge true sind
- **OR** — true, wenn mindestens ein Eingang true ist
- **XOR (exclusive OR)** — true, wenn genau ein Eingang true ist (bei beiden true → false)

### Was hat mich überrascht?
- Transistoren funktionieren wie ein **Wasserhahn**: Mit dem kleinen Steuerdraht-Strom (Hand am Hahn) kontrolliert man einen viel größeren Strom (Wasser, das durchfließt). Dieses simple Prinzip ist die Basis aller Computer.

## Folge 4: Representing Numbers and Letters with Binary

### Kernideen
- Computer arbeiten in **Bit-Blöcken fester Größe** (8, 32, 64 Bit) — die Blockgröße bestimmt, welche Werte maximal darstellbar sind
- Negative Zahlen und Kommazahlen erfordern **Konventionen zur Interpretation** — der Computer "weiß" nicht, ob eine Zahl negativ ist, sondern liest sie nach Regel
- **Unicode hat ASCII abgelöst**, weil 8 Bit für nicht-westliche Sprachen (Mandarin, Japanisch) nicht ausreichten

### Konzepte / Begriffe, die neu für mich waren
- **Byte** — 8 Bit, kann 256 verschiedene Werte darstellen (0–255)
- **8-Bit-Computer / 8-Bit-Grafik** — verarbeitet Daten in 8-Bit-Einheiten, daher z.B. nur 256 Farben darstellbar
- **32-Bit-Computer** — max. darstellbarer Wert ≈ 4,3 Milliarden (2³²)
- **64-Bit-Computer** — max. darstellbarer Wert ≈ 9,2 Quintillionen (2⁶⁴); Standard in heutigen PCs
- **Vorzeichen-Bit (naive Variante)** — erstes Bit signalisiert Vorzeichen (0 = positiv, 1 = negativ); in der Praxis nutzen Computer meist Two's Complement (effizienter)
- **Floating Point** — Zahlen mit "fließendem Dezimalpunkt"; ermöglicht sehr große und sehr kleine Werte mit fester Bit-Anzahl
- **IEEE 754-Standard** — internationaler Standard zur Darstellung von Floating-Point-Zahlen
  - 32-Bit Float: 1 Bit Vorzeichen, 8 Bit Exponent, 23 Bit Signifikand
- **ASCII** — amerikanischer Standard zur Codierung von Zeichen als Zahlen (8 Bit → 256 Zeichen)
- **Multibyte-Codierung** — Notlösung in asiatischen Ländern, weil ASCII für Sprachen mit tausenden Zeichen nicht ausreichte
- **Unicode** (1992) — universelles Codierungssystem, 16 Bit pro Zeichen, Platz für >1 Mio. Zeichen; löste das Babel der nationalen Codierungen ab

### Was hat mich überrascht?
- Binär-Codierung wird nicht nur für Buchstaben (ASCII/Unicode) verwendet, sondern auch für **Sounds (MP3), Farben (Pixel), Bewegtbild (GIF)**. Alles, was wir digital konsumieren, ist letztlich eine Folge von Zahlen — und Zahlen sind letztlich Bits.

## Zusammenhang zu meiner Backend-Reise
- **Boolean Operatoren in jedem C#-Code:** Was ich später als `if (a && b)` oder `x || y` schreibe, sind dieselben AND/OR-Operationen, die in den Logic Gates physikalisch passieren. Mein Code ist nur die hohe Abstraktionsebene davon.
- **Encoding-Bugs verstehen:** Wenn ich später bei einer Web-API einen `string` aus der Datenbank lese und Sonderzeichen falsch ankommen ("café" wird zu "café"), liegt das an falscher Encoding-Behandlung (UTF-8 vs. Latin-1 vs. Unicode). Folge 4 ist die Basis, um solche Bugs überhaupt zu verstehen.
- **Datentyp-Wahl im Code:** Wenn ich in C# zwischen `int`, `long`, `float`, `double` wähle, treffe ich konkrete Entscheidungen über Bit-Größe und Genauigkeit — direkt aus dieser Folge.
















# Meine Version
# Crash Course CS — Folge 3 + 4

## ! Sehr Wichtig !
## Folge 3: Boolean Logic & Logic Gates

### Kernideen
- Computer basieren auf einem Binärsystem von 1 und 0, was 2 Zustände sind, und zwar True und False
- Binärsysteme arbeiten mit der Boolschen Algebra um komplexe Operationen berechnen zu können auf Zustandsebene
- Transistoren können diese Zustände und Operationen perfekt nachstellen

### Konzepte / Begriffe, die neu für mich waren
- **2 Zustände im Computer** - der eingeschaltete Zustand in dem Strom fließt, representiert *"true"* und der augeschaltete Zustand, in dem kein Strom fließt reprsentiert *"false"*
- **Ternary - 3 Zustände**
- **Quinary - 5 Zustände**
- **Boolean Algebra** - hier sind Werte der Variablen Wahr und Falsch und die Operationen logisch
- **3 fundamentale Operationen der Boolschen Algebra** - "NOT", "AND" und "OR"
- **NOT** - negiert Werte z.B aus Wahr -> Falsch und aus Falsch -> Wahr
- **Transistor Funktion** - hat einen Steuerdraht (engl. Control Wire) und 2 Elektrode. Der Streuerdraht agiert als Input und die untere Elektrode als Output. Mit einem Transistor hat man einen Eingang und einen Ausgang.
-> Wenn man den Eingang/Input einschaltet wird auch der Ausgang/Output eingeschaltet, weil Strom durch ihn fließen kann, und genauso wenn man ihn auschaltet.
-> Schaltkreis kann modifiziert werden um z.B. Operationen zu schaffen wie "NOT"
- **Gatter (engl. Gates)** - man sagt z.B "NOT-Gates"/"NICHT-Gatter", da sie den Pfad des Stromes steuern
- **AND** - nur wahr/true, wenn beide Werte gleich sind
- **OR** - wahr/true, wenn mindestens einer der beiden Zustände wahr ist
- **XOR (= exclusive OR)** - wie "OR" eigentlich, mit einer Ausnahme, dass wenn beide Werte wahr/true sind ein false als output kommt, also nur ein Wert darf true sein
- **TRUE & FALSE** - erste Repräsentation von Daten

### Was hat mich überrascht?
- Das Transistoren vergleichbar mit einem Wasserhahn funktionieren bei dem der Hahn auf- und zu gedreht werden kann

## Folge 4: Representing Numbers and Letters with Binary

### Kernideen
- Mehre Zahlensysteme mit denen man beliebig große Zahlen darstellen kann, hier Binärsystem und Dezimalsystem
- Negative und Fließkommazahlen im Binärsystem
- Mit dem ASCII Code werden Buchstaben durch Zahlen dargestellt und Unicode ist die universell genutzte Variante

### Konzepte / Begriffe, die neu für mich waren
- **8-Bit-Computer** - erledigt die meisten ihrer Operationen in 8-Bit-Einheiten, also von 0-255, somit 256 verschiedene Werte
- **8-Bit-Grafik** - ist auf 256 verschieden Farben für ihre Grafiken beschränkt
- **Byte** - 1 Byte sind 8 Bit
- **32- und 64-Bit-Computer** - diese Computer areiten mit 32- oder 64-Bit-Blöcken, z.B. dieg rößte Zahl die man mit 32 Bit darstellen kann ist knapp 4,3 Milliarden -> entspricht 32x 1er im Binärsystem
- 64-Bit-Computer** - der größter Wert, den man mit einer 64-Bit-Zahl darstellen kann, ist ca. 9,2 Quintillionen
- **negative Binärzahlen** - meisten Computer verwenden das erste Bit für das Vorzeichen: 
1 für negative, 0 für positive Zahlen
- **Floating Point Numbers** - wird "Fließkommazahlen" genannt, da der Dezimalpunkt "herumfließen" kann irgendwo mitten in einer Nummer
- **IEEE 754-Standard** -  dieser Standard speichert Dezimalwerte in der "wissenschaftlichen Notation" z.B. kann 625.9 geschrieben werden als 0.6259 * 10^3
- **32-Bit Floating Point Number** - bei einer 32-Bit-Fließkommazahl wir das erste Bit für das Vorzeichen der Zahl verwendet (positiv/negativ), die nächsten 8 Bit werden zum Speichern des Exponenten und die verbleibenden 23 Bit zum Speichern der Signifikanten
- **ASCII Code** - dem amerikanischen Standardcode für den Informationsaustausch
- **Probleme mit ASCII Code in asiatischen Länder** - Länder wie Asien, Griechenland etc. entwickelten Multibyte-Codierungsschemata, da Sprachen wie mandarin oder japanisch tausende von Zeichen hatten und es keine Möglichkeit gab all diese Zeichen in 8 Bit zu kodieren
- **Unicode** - 1992 entwickelt, um alle verschiedenen internationalen System abzuschaffen und durch eine universelle Kodierung zu ersetzen, 16 Bit mit einem Raum für über 1 mio Codes, genug für alle Zeichen und Sprachen

### Was hat mich überrascht?
- wie ASCII ein Schema für Kodierung von Buchstaben als Binärzahlen definiert, verwenden andere Dateiformate - wie MP3s oder GIFs - Binärzahlen, um Klänge oder Farben eines Pixels in unseren Fotos, Filmen und unserer Musik zu kodieren

## Zusammenhang zu meiner Backend-Reise
- **Boolsche Algebra** - hier sind Werte der Variablen Wahr und Falsch und die Operationen logisch, dass wäre dann relevant zu wissen für logikbasiertes Programmieren
- **ASCII Code bzw- Unicode** - um verschiedenste Zeichen darstellen zu können durch Codierungen
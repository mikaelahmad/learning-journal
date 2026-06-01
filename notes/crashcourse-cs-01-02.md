# KI Version
# Crash Course CS — Folge 1 + 2

## Folge 1: Early Computing

### Kernideen
- Der Begriff "Computer" war ursprünglich eine **Berufsbezeichnung** (Mensch, der rechnet, ab ca. 1613), erst später ein Gerät
- Die Entwicklung von Rechenmaschinen wurde fast immer durch **bürokratische oder militärische Notwendigkeit** vorangetrieben — nicht durch reine Forschung
- Babbages "Analytical Engine" (Konzept, 1830er) hatte bereits die Grundarchitektur jedes modernen Computers: **Programm + Speicher + Output**

### Konzepte / Begriffe, die neu für mich waren
- **Abakus** — erste Rechenmaschine, ~4000 Jahre alt
- **Astrolabium** — Navigationshilfe für Seefahrer (Himmelsrichtungen)
- **Rechenschieber** — analoges Werkzeug für Multiplikation/Division
- **Zahlenregister** — vorberechnete Tabellen, um langwierige Berechnungen zu ersparen (z.B. Artillerie-Tabellen bis 2. Weltkrieg)
- **Difference Engine** (Babbage, 1823) — mechanische Polynom-Rechenmaschine, nie fertiggestellt, 1991 nachgebaut → funktionierte
- **Analytical Engine** (Babbage) — Konzept des ersten General-Purpose-Computers (Programme, Speicher, Drucker-Output)
- **Hollerith-Tabelliermaschine** (1890) — elektromechanisch, 10× schneller als Handarbeit, ermöglichte US-Volkszählung in 2.5 statt 13 Jahren → Beginn der kommerziellen Computer-Nutzung
- **IBM** — entstand 1924 aus Holleriths Tabulating Machine Company

### Was hat mich überrascht?
- Die kommerzielle Computer-Industrie hat ihren Ursprung in einer **Volkszählung**, nicht in Forschung oder Militär

## Folge 2: Electronic Computing

### Kernideen
- Computer-Entwicklung ist im Kern die Geschichte des **schnelleren Schaltens zwischen zwei Zuständen** (An/Aus)
- Jede Generation (Relais → Vakuumröhre → Transistor) wurde **kleiner, schneller, zuverlässiger** und ermöglichte die nächste Stufe der Computer
- Bevölkerungswachstum, Weltkriege und Bürokratie schufen den Druck für Automatisierung

### Konzepte / Begriffe, die neu für mich waren
- **Relais** — elektrisch gesteuerter mechanischer Schalter; langsam, verschleißt
- **Vakuumröhre** (1904) — Schalter ohne bewegliche Teile, tausendfach schneller als Relais, aber heiß und groß
- **Transistor** (1947, Bell Labs) — winzig, schnell, langlebig, kein Hitzeproblem; aus Halbleitern (meist Silizium)
- **Halbleiter** — Material, das je nach Bedingung leitet oder nicht leitet → Grundlage des Transistors
- **Bug** — Begriff stammt aus einer echten toten Motte (1947) in der Harvard Mark 1
- **Silicon Valley** — Name kommt vom Silizium (engl. silicon) für Halbleiter; Ursprung in Shockleys Firma → Fairchild → Intel

### Was hat mich überrascht?
- Moderne Transistoren sind **<50 Nanometer** groß — ein Blatt Papier ist 100.000 Nanometer dick. Auf einem CPU-Chip sitzen Milliarden davon.

## Zusammenhang zu meiner Backend-Reise
- **Schaltgenerationen** (Relais → Röhre → Transistor): erklärt, warum heutige Computer überhaupt so schnell sind — sie schalten Milliarden Zustände pro Sekunde. Dieses Bild hilft mir später, Performance-Themen zu verstehen (Cache vs. RAM, CPU-Architektur).
- **Babbages Analytical Engine** hatte schon das Modell *Programm + Speicher + Output*. Genau das schreibe ich später auch im Backend: Eingabe → Verarbeitung → Speicher → Ausgabe. Die Architektur ist 200 Jahre alt.
- **Computer entstanden aus Bedarf nach Datenverarbeitung** (Volkszählung, Kriege). Backend-Entwicklung ist heute genau dasselbe — Daten effizient verarbeiten. Ich bin Teil derselben 150-jährigen Geschichte.
























# Meine Version
# Crash Course CS — Folge 1 + 2

## Folge 1: Early Computing

### Kernideen
- Woher eigentlcih Computer kommen die wir so selbstverständlich in unser Leben integriert haben und was mit dem Begriff Computer auf sich hat
- die ersten Computer bzw. Rechenmaschinen gab es schon vor über 4000 Jahren um Arbeit in der Gesellschaft zu erleichtern
- Nutzung von Zahlen der Strategie von Kriegen
- Charles Babbage undAda Lovelacke beides Wissenschaftler die ihrer Zeit voraus waren und der heutigen Informatik viel mitgegeben haben
- Herman Hollerith der die Nutzung von Computer Populär gemacht hat und als Mitbegründer vom heutigen bekannten IBM bekannt ist

### Konzepte / Begriffe, die neu für mich waren
- Transistoren
- der erste Computer Abakus bzw. erste Rechenmaschine
- Astrolabium zur Feststellung von Himmelsrichtungen für Seefahrer
- Rechenschieber als Hilfestelllung bei Multiplikationen und Divisionen
- Begriff Computer das erste mal 1613 -> hier als Berufsbezeichnung -> Ein Computer war eine Person die davon lebte Berechnungen zu machen manchmal mit der Hilfe von Maschinen
- leibnizsche Rechenmaschine 1694
- im 20. Jahrhundert wurden anfangs Zahlenregister geführt um große Quadratzahlen nicht mit einer Rechenmaschine berechnen zu müssen, da dies Tage dauern würde. Auch für Soldaten wurden Register zusammengestellt um bei Attelerie Umgebungsbedingungen, Zieldistanz und optimalen Winkel für eine Kanone zu erhalten um ein Ziel zu treffen. Wurde bis zum 2.Weltkrieg benutzt. Problem bei neuer Architektur von Attelerie musste ein ganz neues Register erstellt werden, sehr ineffizient
- 1823 startete Charles Babbage das Projekt "Difference Engine" eine komplexe Maschine die mit Polynomen arbeitet (Polynome => meint man das Verhältnis zwischen 2 verschiedenen Variablen wie Reichweite und Luftdruck) was über 2 Jahrzente ging.
Das Projekt wurde fallengelassen, jedoch 1991 wieder von Histoikern nach Babbages Plan fertig gestellt und die Maschine hat funktioniert
- Charles Babbage "Vater der Informatik", kam dann während dem Bau der difference Engine auf die "Analytical Engine" welche eine Maschine für den allgemeinen Gebrauch ist, wie übergeben und abspielen von Programmen, hat einen Speicher und sogar einen primitiven Drucker
- Ada Lovelace "Erste Programmiererin" schrieb fiktive Programme für dei Analytical Engine
- Computer wurden kaum im Alltag genutzt im 19. Jahrhundert, jedoch 1890 gab es eine Volkszählung in der USA welche alle 10 Jahre durchgeführt werden muss, jedoch war diesmal die USA überbevölkert und die Volkszählun würde voraussichtlich 13 Jahre dauern jedoch ist die Volkszählung alles 10 Jahre deshalb braucht man ein Rechenmaschine die das schneller schafft
Dafür wandten die zuständigen Behörden sich an Herman Hollerith der eine elektro-mechanische Tabelliermaschine gebaut hatte welche die schnelligkeit verzehnfacht hatte und somit die Volkszählung innerhalb von 2.5 Jahren durchgeführt hatte
Somit erkannte die Arbeitswelt den Wert von Computern und sah das Potential Arbeiten mit Informationen wie Buchführung, Versicherungswesen und Lagerbestände zu optimimieren und zu erleichtern
Nachfrage sprang in die Höhe
- Um Nachfragen nachzukommen, gründete Herman Hollerith die Tabulating Machine Company. 1924 schloss sich das Unternehmen mit anderen Maschinenherstellern zusammen und somit kam es zur "IBM" International Business Machines Corporation

### Was hat mich überrascht?
- Herman Hollerith ein großer Mitbegründer der IBM ist, der dadurch Groß wurde dass es in der USA eine Volkszählung 1890 gab für die man einen leistungsfähhigen Rechner gebraucht hatte.

## Folge 2: Electronic Computing

### Kernideen
- Der Wechsel von Relais zu Elektronenröhren zu Transistoren, die es ermöglicht haben Elektrizität immer schneller an und auszuschalten bzw. 2 Zustände immer schneller verändern zu können
- Einfluss von der Umwelt auf die Entwicklung von Computern
- Große Persönlichkeiten die verantwortlich sind für die Erfindungen 

### Konzepte / Begriffe, die neu für mich waren
- Weltbevölkerung hat in der ersten Hälfte ds 20. Jahrhundert drastisch zugenommen
- im 1. Weltkrieg wurden über 70 mio Menschen mobilisiert und im 2. Weltkrieg über 100 mio
- erstmals begannen Menschen sich ernsthaft Gedanken über das Bereisen von Planeten zu machen
- Zuwachs von Komplexität, Bürokratie und Daten führte zu einem wachsenden Trieb nach Automatisierung und Algorithmen
- Einer der größten gebaute elektro-mechanischen Computer, ist der Harvard Mark 1 1944 von IBM, im Auftrag der Alliierten im 2. Weltkrieg 
- 1947 fanden Arbeiter an der Harvard Mark 1 eine totte Motte bzw. ein Insekt in einem nicht funktionierenden Relay (= elektrisch gesteuerte mechanische Schalter die einen Stromfluss an einer bestimmten Stellen an- und abschalten kann), Grace Hopper sagte dann "Von da aus, wann immer etwas nicht in einem Computer funktioniert, dann sagten wir es hätte Insekten drinnen ("BUGS")"
-> somit entstand der Begriff "Bugs" für Fehler im Computer
- 1904 Physiker John Ambrose Fleming entwickelte er die Elektronenröhre, es ist im Grunde ein Relai aber wichtigerweise haben Elektronenröhren keine beweglichen Teile. Das bedeutet weniger Verschleiß, und noch wichtiger, sie könnten tausende Male pro Sekunde geschaltet werden.
-> Diese Trioden-Vakuum-Röhren sollten später die Grundlage für Radio, Telefonieren über lange Distanzen, und viele ander elektronische Geräte für fast ein halbes Jahrhundert werden 
- Der erste großflächige Einsatz von Elektronenröhren war der Collossus Mark 1, entworfen von Tommy Flowers 1943 in England um Nazi-Funksprüche zu entschlüsseln
- 1947 erfanden Wissenschaftler John Bardeen, Walter Brattain und William Shockley der Transistor und mit ihm wurde eine ganz neue Ära des Computers eingeleitet
- Ein Transistor ist wie ein Relay oder eine Elektronenröhre - er ist ein Schalter der geöffnet oder geschlossen werden kann, wenn elektrischer Strom an einem Kontrolldraht angelegt wird. 
- ein Halbleiter
- das führte zu kleiner und kostengünstigeren Computern, wie dem IBM 608, der in 1957 eingeführt wurde
- Heutzutage verwenden Computer Transistoren, die kleiner als 50 Nanometer groß sind
- Transistoren sind nicht nur super klein sie können auch Zustände millionenfach pro Sekunden umschalten, sind super schnell und können jahrzentelang laufen
- da das meistbeutze Material um Halbleiter herzustellen Silizium ist (engl. Silicon) wurde die Region bald als "Silicon Valley" bekannt
- William Shockley mitbegründer des Transistors zog auch zum Silicon Valley und gründete dort die Firma "Shockley Semiconductor", deren Mitarbeiter "Fairchild Semiconductors" gründeten und deren Mitarbeiter wiederum die Heutbekannte "Intel"- die weltgrößte Computer-Chip-Hersteller-Firma gründeten


### Was hat mich überrascht?
- Heutzutage verwenden Computer Transistoren, die kleiner als 50 Nanometer groß sind - zum Vergleich ein Blatt Papier ist ca 100.000 Nanometer dick

## Zusammenhang zu meiner Backend-Reise
- Um die Fundamente der Informatik kennenzulernen, zu verstehen wie es alles angefangen hat und worauf die Informatik aufbaut, um somit sich leichter Vetraut machen zu können

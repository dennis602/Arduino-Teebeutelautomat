# Arduino-Teebeutelautomat
## Informatik-Projekt von Peter und Dennis, 12ab

## Inhaltsverzeichnis

[Vorwort](#1)

[Projektentwicklung](#2)

[Unser Projekt](#3)

[Unsere Hardware](#4)

[Unsere Software](#5)

[Schlusswort](#6)

[Quellen](#7)
 
## <a name="1"></a>Vorwort

Im unserem ersten Projekt hatten wir sehr gute Erfahrungen Mit Arduino gemacht. Deshalb wollten wir disesmal auch gerne wieder mit dieser Soft- und Hardware arbeiten. Da unser Parkhaus aber nicht genug Potential bot, mussten wir uns etwas neues ausdenken, um den Anforderungen für dieses Halbjahr grerecht zu werden. Denn jetzt sollten wir vom Programmieren her anspruchsvoller und versierter werden. Da es mit Arduino aber noch zahlreiche weitere und auch durchaus anspruchsvollere Möglichkeiten gibt, entschieden wir uns schlussendlich dafür, beim Arduino zu bleiben. Dann haben wir erstmal, ohne uns groß Gedanken über unser Projekt zu machen, rumprobiert und sind schließlich an fogenden neuen  Elementen hängengeblieben: Taster, Stepper-Motor, Motor-Shield, Mega-Arduino und einem Summer/Pieper. Daraus wollten wir dann eine Teebeutelmaschine machen. Eine Tasse wird auf einen Platz gestellt und sobald dies ein Ultraschallsensor erkennt und ein Taster für einen zur Wahl stehenden Modus gedrückt wird. Dann fährt ein bestimmts Programm ab. Zuerst wird ein Teebeutel in die Tasse getunkt, während der Zieh-Zeit wird er einige Male hoch und runterbewegt, sobald er fertig ist, ertönt ein Signalton und zum Schluss fährt eine Konstruktion über die Tasse, auf die dann der Beutel fallen kann. Wir konnten unser großes Projekt also wieder aus mehreren kleineren Aufbauen, was ja auch letztes Mal schon das Prinzip unserer Arbeit war.
Einige Grundsätzliche Bauteile und Softwareelemente haben sich natürlich seit dem letzten Projekt nicht verändert, deshalb werden wir diese nicht nocheinmal erklären. Dies haben wir bereits in der Projekteseite für das Arduino-Parkhaus getan. https://github.com/dennis602/Projektseite-Arduino-Parkhaus/blob/master/README.md


## <a name="2"></a>Projektentwicklung

Wie im Vorwort beschrieben wollten wir gerne beim Arduino für das Informatikprojekt des zweiten Halbjahres bleiben. Allerdings kannten wir uns anders als im ersten Projekt schon mit Arduino aus und mussten so die Grundlagen nicht nochmal erlernen. Da uns trotzdem noch gar nicht klar war, was man eigentlich alles mit dem Arduino machen kann und wie viele Möglichkeiten es gibt, bestand unsere Arbeit in den ersten Wochen darin, uns mit diesen Möglichkeiten auseinanderzusetzen. Wir haben herumexperimentiert mit Tastern, Motorshields, Motoren, Steppermotoren, Transistoren, Potentiometern und vielem mehr. Schlussendlich einigten wir uns vorläufig auf die Idee eine Teebeutelmaschine zu entwerfen. Um eine externe Stromversorgung zu gewährleisten, die den Mikrocontroller nicht gefährdet, lag unser Fokus zuerst auf dem Motorshield. sobald damit alles funktioniert hat, kam der Steppermotor an die Reihe. Dieser lässt sich wesentlich leichter und dabei flüssiger als ein konventioneller Motor ansteuern. Das ganze Projekt über haben wir dann immer Teilschritte entworfen und diese ins Gesamte eingefügt. An dem Projekt haben wir Schlussendlich immer nur in "rohform" gearbeitet, also die Hardware immer nur pragmatisch zusammengebaut, ohne auf Konstruktionen oder finale Versionen zu achten. So haben wir im Laufe der Zeit eigentlich immer in Teilschritten gearbeitet, diese mit dem Serial-Print überwacht und schlussendlich zum Gesamten hinzugefügt. Natürlich hat dann Corona seinen Teil beigetragen und unsere Pläne durcheinandergebracht. So haben wir am letzten Schultag alles mitgenommen und von zuhause gearbeitet. Da ein Treffen auch nicht wirklich kontruktiv war, hat dann einer alleine den Sketch finalisiert und die Lego Konstruktion gebaut.
Im ganzen hat also eigentlich alles sehr gut funktioniert, doch durch Corona mussten wir improvisieren. Mit dem Endergebniss sind wir sehr zufrieden.



## <a name="3"></a>Unser Projekt

Wir haben jetzt also einen Teebeutelautomaten, der drei Knöpfe für drei verschiendene Teesorten und einen Knopf zum Beenden des Teezubereitens hat. Nimmt man die Tasse weg, bewegt sich von selbst eine Schale unter den Teebeutel, auf den dieser abtropfen kann.

In dem folgenden Video sieht man einen beispielhaften Ablauf von unserem Teebeutel-Automaten.

Video: https://www.youtube.com/watch?v=UV_n-1Byzow


![Titelbild Youtube](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Fot%20Thumbnail%20tee.PNG?raw=true)

Unser Sketch ist bei diesem Projekt zu lang, um ihn in Teilstücken ganz zu erklären. Hier ist der Sketch als ganzes zu sehen und jede neue Funktion ist an der Seite erkärt:

![Sketch](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Sketch)


## <a name="4"></a>Unsere Hardware

Auf dem folgendem Bild sieht man unsere ausgebreitete, nicht eingebaute Hardware mit Nummern versehen.
 
![Bild Hardware nummeriert](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Foto%20Nummer%20Tee.PNG?raw=true)
 
### 1) Netzgerät

Dieses ist mit einer Steckdose verbunden und bietet die Möglichkeit, die ausgegebene Spannung manuell zu verändern. Durch die zwei angeschlossenen Kabel können wir über das Motorshield den Steppermotor mit Strom versorgen.

### 2) Breadboard mit Tastern
Es bildet eine Erweiterung für den Mikrocontroller, da es für uns die Möglicheit bietet alle anderen Geräte mit Strom zu versorgen, obwohl der Mikrocontroller nur einen einzigen 5V Anschluss hat. Dazu verbindet man einfach den 5V Anschluss mit der Plus-Leiste des Breadboards und die Minus-Leiste mit GND (Groundpin am Mikrocontroller). Anschließend konnten wir alle weiteren Geräte an diese beiden Leisten anschließen und mit Strom versorgen. Außerdem kann man weitere externe Geräte mit dem Microcontroller oder miteinander verbinden. Ein ähnliches Breadboard haben wir im ersten Projekt auch schon verwendet, dieses ist einfach nur größer. https://github.com/dennis602/Projektseite-Arduino-Parkhaus/blob/master/README.md



### 3) Arduino MEGA Mikrocontroller
Der Arduino funktioniert prinzipell genauso wie ein normaler Mikrocontroller. Somit gilt für ihn ebenfalls: Er ist das Herzstück von Arduino, da er Software mit Hardware verbindet. Auf ihn wird der Sketch übertragen und an ihn angeschlossen sind alle externen Geräte. in unserem Fall sind das alle nachfolgenden Geräte, ausgenommen der Steppermotor, der nur indirekt über das Motorshield mit dem Mikrocontroller verbunden ist. Der vorteil des Arduino Mega ist, dass es mehr Ausgänge bietet al der herkömmliche Mikrocontroller. Insgesamt sind es 54 digitale Pins, 16 anloge Inputs und 4 serielle Ports.

### 4) Motorshield
Um einen Motor präzise steuern zu können, haben wir uns mit dem sogenannten Arduino Motorshield beschäftigt. Dieses ist ein weiteres Board, welches man auf den Mikrocontroller aufstecken kann. 

![Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Motorshield%20Demobild.jpg?raw=true)

Da wir aber weiterhin die Ports des Mikrokontrollers nutzen wollten, haben wir nur die nötigen Ports per Kabel mit dem Motorshield verbunden. 

Das Motorshield besitzt mehrere Anschlüsse für DC-Motoren (Gleichstrommotoren), Steppermotoren (Schrittmotoren, s. ...) und Servos. Man kann eine externe Stromquelle zwischen 5 und 12 Volt anschließen, um den Mikrocontroller zu entlasten.

Um das Motorshield im Sketch einzubauen, muss man vorher die entsprechende Bibliothek aus dem Internet herunterladen und sie per "#include <AFMotor.h>" einbinden. Von nun an gibt es feste Befehle, mit denen man den Motor sehr genau und präzise steuern kann. 

![Sketch Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/includeAFMotor.PNG?raw=true)

### 5) Ultraschallsensor
Der Ultraschallsensor (HC-SR04 misst Entfernungen zu Objekten auf Grundlage von ausgesendeten Schallwellen und der Schallgeschwindigkeit. Der Ultraschallsensor hat vier Anschlüsse: Zum einen zwei zur Stromversorgung. Dann hat er allerdings noch einen trigPin (Trigger Pin), durch den der Sensor vom Mikrocontroller das Signal bekommt, eine Ultraschallwelle zu senden. Der letzte Anschluss ist ein Echo Pin, der durch den Empfang der reflektierten Ultraschallwelle ein Signal zum Mikrocontroller zurücksendet. Der Mikrocontroller berechnet anschließend die Entferung zum Objekt. In unserem Projekt misst der Ultraschallsensor den Stellplatz der Tasse aus, und nur, wenn erkannt wird, dass dort etwas steht, kann der Rest funktionieren. (Taster und Teebeutelbewegung)

### 6) LCD-Display
Das Flüssigkristall-Display kann aus elektrischen Signalen visuelle machen und überträgt hierzu vorher festgelegte Zeichen auf einen Bildschirm. In unserem Fall fungiert das Display als Kommamdogeber an den Benutzer und ls Statusanzeige. Zum einen wird gesagt, was man zu tun hat. Zum Beispiel "Bitte Tee wählen" oder "drücke fertig". Zum anderen wird angezeigt, wie viele Umdrehungen der Teebeutel noch braucht( "Warte bis 4") oder dass der Tee nun fertig ist.

Wir haben ein sogenanntes I2C-Display, was die Arbeit deutlich vereinfacht. Man braucht nur vier Kabel. Zwei für die Stromversorgung und zwei für die Kommunikation mit dem Mikrocontroller (SDA und SCL). Jedes LCD-Display hat eine eigene "Adresse". Diese kann man mithilfe eines Adressenscanners herausfinden (s. ![hier](https://github.com/dennis602/Stundenprotokoll-II/blob/master/README.md#30) im Protokoll).

Anschließend kann man das Display im Sketch programmieren, indem man drei Bibliotheken einbindet. Wie das Ganze funktioniert, sieht man auf folgendem Screenshot:

![LCD Erklärung](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/LCD_Erkl%C3%A4rung.PNG?raw=true)

Für die Kontrasteinstellung auf dem Display gibt es hinten ein kleines schon verbautes Potentiometer, an dem man drehen kann.

### 7) Steppermotor
Der Steppermotor ist eine Art der Elektromotoren. Es handelt sich um einen Synchronmotor, der durch mehrere innere Spulen ein rotierendes Magnetfeld erzeugt und so eine Umdrehung in 2048 sehr feine Schritte aufteilen kann. Er entwickelt zwar eine relativ langsame Drehgeschwindigkeit, dafür aber ein hohes Drehmoment. 

Durch die Aufteilung in 2048 Schritte ist die Steuerung sehr exakt. Im Sktech führt man ihn mit "AF_Stepper" ein, legt im Void Setup per "motor.setSpeed()" eine Geschwindgkeit fest und kann im Void Loop durch "motor.step()" festlegen, wie viele der 2048 Schritte er machen soll und, ob er vorwärts oder rückwärts drehen soll.

![Sketch Stepper](https://github.com/dennis602/Stundenprotokoll-II/raw/master/Code_motorshield_1.PNG?raw=true)

Damit ist er für unser Projekt bestens geeignet.


### 8) Piezosummer

Ein Piezosummer sendet auf Kommando ein akustisches Signal. Theoretisch kann man durch verändern der Spannung (z.B. mit einem Potentiomeer) die Frequenz und damit die Tonhöhe dieses Signals verändern. Unser Summer ist allerdings direkt an den Mikrocontroller angeschlossen und bekommt so durchgängig eine Spannung von 5V. Im Projekt dient das Summen als Signal, dass der Tee nun fertig ist. Daraufhin soll man den Taster "fertig" betätigen und der Servomotor fährt eine Platte über die Tasse.

### 9) Servomotor
Eon Servomotor kann Anweisungen sehr präzise ausführen. Doch er hat nur einen Bewegungsradius von 180 Grad. Durch Kommandos im Sketch bewegt sich dann sehr Servo innerhalb dieser 180 Grad Spanne vor und zurück. Im Projekt fährt der Servo eine Platte über die Tasse nd unter den tropfenden Teebeutel, sobald ein bestimmter Taster betätigt wurde.


### 10) Verbindungskabel mit USB-Anschluss
Dieses verbindet den Mikrocontroller mit dem Computer und somit mit dem Arduino-Programm. Es ermöglicht also das Übertragen des Sketches. Außerdem wird über diesen Anschluss die Stromversorgung gewährleistet. Dieses haben wir im ersten Projekt auch schon verwendet. https://github.com/dennis602/Projektseite-Arduino-Parkhaus/blob/master/README.md






## <a name="5"></a>Unsere Software

![Sketch](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Sketch)

### Spezielle Programmiertechniken in unserem Sketch

Man kann sagen, dass wir in diesem Projekt sehr viel mit Variablen gearbeitet haben. Vorwiegend haben wir die "int" Variablen genutzt. Diese sind für unser Projekt völlig ausreichend. Man kann sie mit "int Name" benennen und ihr mit "int Name = Wert" auch einen Wert zuweisen, den sie speichern soll. Hat man das einmal vor dem Loop festgelegt, reicht es im restlichen Sketch, nur den Namen zu schreiben. 

Im übrigen ist "#define" das gleiche wie "const int". Das bedeutet nämlich, dass diese Variable nicht änderbar ist, sondern die ganze Zeit einen Wert behält. 


## 1) Die While-Schleife
 
## 2) Variablen per Knopfdruck erhöhen

Diese Technik haben wir benutzt, um so lange auf dem LCD-Display "Tee ist fertig" stehen zu haben, bis der Nutzer den Tee nimmt und einen Knopf zum Beenden des Vorgangs drückt. An der entsprechenden Stelle im Sketch schreiben wir also, dass der Bilschirm solange "Tee fertig!" anzeigen soll, wie diese Variable unter 1 ist.

Um eine Variable per Knopfdruck zu erhöhen, muss man zuerst natürlich den Taster ganz normal einführen und bennenen. Anschließend führt man eine Variable "val" (= value) ein, auf der man Werte speichern kann. Außerdem benötigt man die Variablen "buttonState" und "ButtonPresses".

![Variablen](https://github.com/dennis602/Stundenprotokoll-II/raw/master/Endknopf%20einf%C3%BChrung.PNG?raw=true)

Im Setup wird dann festgelegt, dass der buttonState der ausgelesene Wert am Taster ist, also einfach, ob er gedrückt wurde.

Im Loop wird bei jedem Durchgang die Variable buttonPresses, die ja die Häufigkeit des Drücken des Knopfes darstellen soll, immer gleich 0 gesetzt. An entsprechender Stelle im Sketch, also bei uns nach dem Durchlaufen des Motors, wird nun festgelegt, dass auf der Variablen val immer gespeichert wird, wie oft der Knopf gedrückt wurde, indem wir sie gleich digitalRead(switchPin) setzen. Außerdem wird programmiert, dass bei jedem Knopfdruck die Variable buttonPresses durch ++ erhöht wird.

![Variable erhöhen](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/val.PNG?raw=true)

Wie wir das Ganze umgesetzt haben kann man ![hier](https://github.com/dennis602/Stundenprotokoll-II/blob/master/README.md#32) in unserem Stundenprotokoll finden.

## <a name="6"></a>Schlusswort




## <a name="7"></a>Quellen

https://www.generationrobots.com/de/401113-arduino-motor-shield-rev-3.html

https://funduino.de/nr-15-schrittmotor

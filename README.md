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

Im unserem ersten Projekt hatten wir sehr gute Erfahrungen Mit Arduino gemacht. Deshalb wollten wir disesmal auch gerne wieder mit dieser Soft- und Hardware arbeiten. Da unser Parkhaus aber nicht genug Potential bot, mussten wir uns etwas neues ausdenken, um den Anforderungen für dieses Halbjahr grerecht zu werden. Denn jetzt sollten wir vom Programmieren her anspruchsvoller und versierter werden. Da es mit Arduino aber noch zahlreiche weitere und auch durchaus anspruchsvollere Möglichkeiten gibt, entschieden wir uns schlussendlich dafür, beim Arduino zu bleiben. Dann haben wir erstmal, ohne uns groß Gedanken über unser Projekt zu machen, rumprobiert und sind schließlich an fogenden neuen  Elementen hängengeblieben: Taster, Stepper-Motor, Motor-Shield, Mega-Arduino, einem Summer/Pieper und einem LCD-Display. Daraus wollten wir dann eine Teebeutelmaschine machen. Eine Tasse wird auf einen Platz gestellt und sobald dies ein Ultraschallsensor erkennt und ein Taster für einen zur Wahl stehenden Modus gedrückt wird. Dann fährt ein bestimmts Programm ab. Zuerst wird ein Teebeutel in die Tasse getunkt, während der Zieh-Zeit wird er einige Male hoch und runterbewegt, sobald er fertig ist, ertönt ein Signalton und zum Schluss fährt eine Konstruktion über die Tasse, auf die dann der Beutel fallen kann. Wir konnten unser großes Projekt also wieder aus mehreren kleineren Aufbauen, was ja auch letztes Mal schon das Prinzip unserer Arbeit war.
Einige Grundsätzliche Bauteile und Softwareelemente haben sich natürlich seit dem letzten Projekt nicht verändert, deshalb werden wir diese nicht nocheinmal erklären. Dies haben wir bereits in der Projekteseite für das Arduino-Parkhaus getan. https://github.com/dennis602/Projektseite-Arduino-Parkhaus/blob/master/README.md


## <a name="2"></a>Projektentwicklung

Wie im Vorwort beschrieben wollten wir gerne beim Arduino für das Informatikprojekt des zweiten Halbjahres bleiben. Allerdings kannten wir uns anders als im ersten Projekt schon mit Arduino aus und mussten so die Grundlagen nicht nochmal erlernen. Da uns trotzdem noch gar nicht klar war, was man eigentlich alles mit dem Arduino machen kann und wie viele Möglichkeiten es gibt, bestand unsere Arbeit in den ersten Wochen darin, uns mit diesen Möglichkeiten auseinanderzusetzen. Wir haben herumexperimentiert mit Tastern, Motorshields, Motoren, Steppermotoren, Transistoren, Potentiometern und vielem mehr. Schlussendlich einigten wir uns vorläufig auf die Idee eine Teebeutelmaschine zu entwerfen. Um eine externe Stromversorgung zu gewährleisten, die den Mikrocontroller nicht gefährdet, lag unser Fokus zuerst auf dem Motorshield. sobald damit alles funktioniert hat, kam der Steppermotor an die Reihe. Dieser lässt sich wesentlich leichter und dabei flüssiger als ein konventioneller Motor ansteuern. An dem Projekt haben wir Schlussendlich immer nur in "rohform" gearbeitet, also die Hardware immer nur pragmatisch zusammengebaut, ohne auf Konstruktionen oder finale Versionen zu achten. So haben wir im Laufe der Zeit eigentlich immer in Teilschritten gearbeitet, diese mit dem Serial-Print überwacht und schlussendlich zum Gesamten hinzugefügt. Natürlich hat dann Corona seinen Teil beigetragen und unsere Pläne durcheinandergebracht. So habn wir am letzten Schultag alle mitgenommen und von zuhause gearbeitet. Da ein treffen auch nicht wirklich kontruktiv war, hat dann einer alleine den Sketch finalisiert und die Lego Konstruktion gebaut.
Im ganzen hat also eigentlich alles sehr gut funktioniert, doch durch Corona mussten wir improvisieren. Mit dem Endergebniss sind wai sehr zufrieden.



## <a name="3"></a>Unser Projekt
Wir haben jetzt also einen Teebeutelautomaten, der drei Knöpfe für drei verschiendene Teesorten und einen Knopf zum Beenden des Teezubereitens hat. Nimmt man die Tasse weg, bewegt sich von selbst eine Schale unter den Teebeutel, auf den dieser abtropfen kann.

Video: https://www.youtube.com/watch?v=UV_n-1Byzow
![Video](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Screenshot_Video.PNG?raw=true)


## <a name="4"></a>Unsere Hardware
 Auf dem folgendem Bild sieht man unsere ausgebreitete, nicht eingebaute Hardware mit Nummern versehen.
 
 ![Bild Hardware nummeriert](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Foto%20Nummer%20Tee.PNG?raw=true)
 
### 1) Netzgerät

### 2) Breadboard mit Tastern

### 3) Arduino MEGA Microcontroller

### 4) Motorshield
Um einen Motor präzise steuern zu können, haben wir uns mit dem sogenannten Arduino Motorshield beschäftigt. Dieses ist ein weiteres Board, welches man auf den Mikrocontroller aufstecken kann. 

![Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Motorshield%20Demobild.jpg?raw=true)

Da wir aber weiterhin die Ports des Mikrokontrollers nutzen wollten, haben wir nur die nötigen Ports per Kabel mit dem Motorshield verbunden. 

Das Motorshield besitzt mehrere Anschlüsse für DC-Motoren (Gleichstrommotoren), Steppermotoren (Schrittmotoren, s. ...) und Servos. Man kann eine externe Stromquelle zwischen 5 und 12 Volt anschließen, um den Mikrocontroller zu entlasten.
Um das Motorshield im Sketch einzubauen, muss man vorher die entsprechende Bibliothek aus dem Internet herunterladen und sie per "#include <AFMotor.h>" einbinden. Von nun an gibt es feste Befehle, mit denen man den Motor sehr genau und präzise steuern kann. 

![Sketch Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/includeAFMotor.PNG?raw=true)

### 5) Ultraschallsensor

### 6) LCD-Display
Das LCD-Display ist ein Bildschirm für den Arduino. Auf ihm kann man Textzeilen darstellen. 

Wir haben ein sogenanntes I2C-Display, was die Arbeit deutlich vereinfacht. Man braucht nur vier Kabel. Zwei für die Stromversorgung und zwei für die Kommunikation mit dem Mikrocontroller (SDA und SCL). Jedes LCD-Display hat eine eigene "Adresse". Diese kann man mithilfe eines Adressenscanners herausfinden (s. ![hier](https://github.com/dennis602/Stundenprotokoll-II/blob/master/README.md#30) im Protokoll).

Anschließend kann man das Display im Sketch programmieren, indem man drei Bibliotheken einbindet. Wie das Ganze funktioniert, sieht man auf folgendem Screenshot:

![LCD Erklärung](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/LCD_Erkl%C3%A4rung.PNG?raw=true)

Für die Kontrasteinstellung auf dem Display gibt es hinten ein kleines schon verbautes Potentiometer, an dem man drehen kann.

### 7) Steppermotor
Der Steppermotor ist eine Art der Elektromotoren. Es handelt sich um einen Synchronmotor, der durch mehrere innere Spulen ein rotierendes Magnetfeld erzeugt und so eine Umdrehung in 2048 sehr feine Schritte aufteilen kann. Er entwickelt zwar eine relativ langsame Drehgeschwindigkeit, dafür aber ein hohes Drehmoment. 

Durch die Aufteilung in 2048 Schritte ist die Steuerung sehr exakt. Im Sktech führt man ihn mit "AF_Stepper" ein, legt im Void Setup per "motor.setSpeed()" eine Geschwindgkeit fest und kann im Void Loop durch "motor.step()" festlegen, wie viele der 2048 Schritte er machen soll und, ob er vorwärts oder rückwärts drehen soll.

![Sketch Stepper](https://github.com/dennis602/Stundenprotokoll-II/raw/master/Code_motorshield_1.PNG?raw=true)

Damit ist er für unser Projekt bestens geeignet.


### 8) Summer/Pieper ?????????

### 9) Servomotor

### 10) Verbindungskabel mit USB-Anschluss


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

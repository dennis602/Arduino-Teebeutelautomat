# Arduino-Teebeutelautomat
## Informatik-Projekt von Peter und Dennis, 12ab

kakapopo lol




## Das Motorshield

Um einen Motor präzise steuern zu können, haben wir uns mit dem sogenannten Arduino Motorshield beschäftigt. Dieses ist ein weiteres Board, welches man auf den Mikrocontroller aufstecken kann. 

![Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Motorshield%20Demobild.jpg?raw=true)

Da wir aber weiterhin die Ports des Mikrokontrollers nutzen wollten, haben wir nur die nötigen Ports per Kabel mit dem Motorshield verbunden. 

Das Motorshield besitzt mehrere Anschlüsse für DC-Motoren (Gleichstrommotoren), Steppermotoren (Schrittmotoren, s. ...) und Servos. Man kann eine externe Stromquelle zwischen 5 und 12 Volt anschließen, um den Mikrocontroller zu entlasten.

Um das Motorshield im Sketch einzubauen, muss man vorher die entsprechende Bibliothek aus dem Internet herunterladen und sie per "#include <AFMotor.h>" einbinden. Von nun an gibt es feste Befehle, mit denen man den Motor sehr genau und präzise steuern kann. 

![Sketch Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/includeAFMotor.PNG?raw=true)



## Der Steppermotor

Der Steppermotor ist eine Art der Elektromotoren. Es handelt sich um einen Synchronmotor, der durch mehrere innere Spulen ein rotierendes Magnetfeld erzeugt und so eine Umdrehung in 2048 sehr feine Schritte aufteilen kann. Er entwickelt zwar eine relativ langsame Drehgeschwindigkeit, dafür aber ein hohes Drehmoment. 

Durch die Aufteilung in 2048 Schritte ist die Steuerung sehr exakt. Im Sktech führt man ihn mit "AF_Stepper" ein, legt im Void Setup per "motor.setSpeed() eine Geschwindgkeit fest und kann im Void Loop durch "motor.step()" festlegen, wie viele der 2048 Schritte er machen soll und, ob er vorwärts oder rückwärts drehen soll.

![Sketch Stepper](https://github.com/dennis602/Stundenprotokoll-II/raw/master/Code_motorshield_1.PNG?raw=true)

Damit ist er für unser Projekt bestens geeignet.



Quellen

https://www.generationrobots.com/de/401113-arduino-motor-shield-rev-3.html

https://funduino.de/nr-15-schrittmotor

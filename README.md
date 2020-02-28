# Arduino-Teebeutelautomat
## Informatik-Projekt von Peter und Dennis, 12ab

kakapopo lol




Das Motorshield

Um einen Motor präzise steuern zu können, haben wir uns mit dem sogenannten Arduino Motorshield beschäftigt. Dieses ist ein weiteres Board, welches man auf den Mikrocontroller aufstecken kann. 

![Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/Motorshield%20Demobild.jpg?raw=true)

Da wir aber weiterhin die Ports des Mikrokontrollers nutzen wollten, haben wir nur die nötigen Ports per Kabel mit dem Motorshield verbunden. 

Das Motorshield besitzt mehrere Anschlüsse für DC-Motoren (Gleichstrommotoren), Steppermotoren (Schrittmotoren, s. ...) und Servos. Man kann eine externe Stromquelle zwischen 5 und 12 Volt anschließen, um den Mikrocontroller zu entlasten.

Um das Motorshield im Sketch einzubauen, muss man vorher die entsprechende Bibliothek aus dem Internet herunterladen und sie per "#include <AFMotor.h>" einbinden. Von nun an gibt es feste Befehle, mit denen man den Motor sehr genau und präzise steuern kann. 

![Sketch Motorshield](https://github.com/dennis602/Projektseite-Arduino-Teebeutelautomat/blob/master/includeAFMotor.PNG?raw=true)





Quellen
https://www.generationrobots.com/de/401113-arduino-motor-shield-rev-3.html

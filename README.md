# Sensor-PIR-HC-SR501
Ajuste e instalación de sensor PIR



![download](https://user-images.githubusercontent.com/80070044/169893728-7b3e8fe6-2eae-4be4-9123-a3f4f7899854.jpg)
![arduino-pir-sensor](https://user-images.githubusercontent.com/80070044/169893745-f31b05b9-d4ae-4385-a213-03cfb9658507.png)



Para usarlo con Arduino

El sensor PIR devuelve un estado alto (HIGH) cuando detecta movimiento y un estado bajo (LOW) si no hay nada. Por lo tanto, se gestionará como una entrada digital utilizando la función digitalRead() de Arduino.


![arduino-pir-sensor_bb](https://user-images.githubusercontent.com/80070044/169893901-11a8c1ad-0e6b-483f-8561-fe237be8563d.png)

```C++
//Parameters
const int pirPin  = 2;
//Variables
bool pirStatus  = false;
void setup() {
 //Init Serial USB
 Serial.begin(9600);
 Serial.println(F("Initialize System"));
 //Init digital input
 pinMode(pirPin, INPUT);
}
void loop() {
 readPIR();
}
void readPIR( ) { /* function readPIR */
 ////Test routine for PIR
 pirStatus = digitalRead(pirPin);
 Serial.print(F("Sensor status")); Serial.println(pirStatus);
 if (pirStatus) {
   Serial.print(F("----> Detection"));
   delay(500);
 }
 delay(100);
}


```




Para usarlo con Micro:bit

![download](https://user-images.githubusercontent.com/80070044/169893992-a9c474e0-6fb9-4b1f-af8d-d68dc4bb7a2c.jpg)

![image](https://user-images.githubusercontent.com/80070044/169895984-ba507e06-fa0e-4c48-8273-f33ac6cdfb60.png)

https://makecode.microbit.org/_7FahA4e844mr


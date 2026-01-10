Laboratory Activity #3: Fire Sensor Implementation
Members:
Andino
Llantos
Gomba
Ochoa
Palomar

Objectives:

* Familiarize students with basic sensor components that can be used in IoT.
* Integrate sensor components in an Arduino circuit.
* Create a simple implementation of a fire sensor.

Activity Description:
This laboratory activity involves creating a fire sensor system using a thermistor and a photoresistor connected to an Arduino board.
The system detects temperature and ambient light levels. When the temperature exceeds 50°C and brightness exceeds 220, a red LED on digital pin 12 blinks rapidly to indicate a fire.
Optionally, a buzzer can be added using the same pin as the LED.

Expected Output:
The system continuously monitors temperature and brightness. 
If both readings exceed their thresholds, the LED/buzzer on pin 12 blinks rapidly, signaling a fire.
When readings drop below the thresholds, the LED/buzzer turns off.

Tools and Components Used:
* Hardware: Arduino Uno, Thermistor, Photoresistor, Red LED, Buzzer (optional), Breadboard, Jumper Wires, Resistors
* Software: Arduino IDE
* Diagram Tool: Tinkercad

Code Description:
Pin definitions are set using #define for the thermistor (A0), photoresistor (A2), and LED/buzzer (12).
Threshold values are stored using const int for temperature (50°C) and brightness (220).
readTemperature() function reads the thermistor value and converts it to Celsius using the Beta equation.
readBrightness() function reads the analog value from the photoresistor.
In setup(), the LED/buzzer pin is set as OUTPUT.
In loop():
Temperature and brightness are read from the respective sensors.
If both readings exceed their thresholds, the LED/buzzer blinks rapidly (200 ms ON, 200 ms OFF).
Otherwise, the LED/buzzer stays OFF.

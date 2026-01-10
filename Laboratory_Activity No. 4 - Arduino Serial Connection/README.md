Laboratory Activity #4: Arduino Serial Connection

Members: Andino Llantos Gomba Ochoa Palomar

Objectives:

* Understand and implement Arduino Serial Connection.
* Utilize and familiarize students with different basic Serial connection functions.
* Create a simple circuit that can be controlled using Serial commands.

Activity Description:

This laboratory activity involves creating a light monitoring system using a photoresistor connected to an Arduino board. 
The system reads the ambient light levels and blinks an LED on digital pin 8 when the brightness exceeds a set threshold. Students can control the blinking via the Serial Monitor. 
Typing “stop” (case-insensitive) in the Serial Monitor will stop the blinking.

Expected Output:
The system continuously monitors brightness.
When the brightness exceeds the threshold, the LED on pin 8 blinks repeatedly.
Typing “stop” in the Serial Monitor will stop the blinking.

Tools and Components Used:
* Hardware: Arduino Uno, Photoresistor, Red LED, Breadboard, Jumper Wires, Resistor
* Software: Arduino IDE
* Diagram Tool: Tinkercad

Code Description:
Pin definitions are set using #define for the photoresistor (A0) and LED (pin 8).
Threshold values are stored using const int for brightness (220).
Two boolean variables track the LED behavior: isBlinking for ongoing blinking and stopCommand for stopping the LED via Serial.
In setup():
Serial communication is initialized at 9600 baud.
LED pin is set as OUTPUT.
Instructions are printed in the Serial Monitor.
In loop():
The photoresistor is read and normalized to a 0–250 scale.
If brightness exceeds the threshold and no stop command is given, isBlinking is enabled.
Serial input is continuously checked. If the word “stop” is entered, the LED stops blinking.

If isBlinking is true and blinking is not stopped, the LED blinks with 100 ms ON and 100 ms OFF delays.

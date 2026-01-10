Laboratory Activity #2: Working with Analog Signals

Objectives:

1. Discuss analog signals and their implementation in an Arduino circuit.
2. Understand analog to digital signal conversion using the map() function.

Activity Description:
This laboratory activity builds on Lab 1’s running light circuit but introduces analog control.
LEDs connected to digital pins 8 to 12 are controlled using analogWrite(), allowing variable brightness.
The brightness is set according to the reading from a potentiometer connected to pin A0.
The program uses while loops and an array to set pin modes and control LED brightness. 
LEDs turn on one by one, gradually increasing brightness, then turn off one by one, gradually decreasing brightness. 
The map() function converts the potentiometer’s analog input (0–1023) to a PWM value (0–255).

Expected Output:
LEDs light up sequentially from pin 12 to pin 8, gradually increasing brightness according to the potentiometer, then turn off sequentially with decreasing brightness. 
This cycle repeats continuously with a 1-second delay between each LED.

Tools and Components Used:

* Hardware: Arduino Uno, LEDs, Breadboard, Potentiometer, Jumper Wires, Resistors
* Software: Arduino IDE
* Diagram Tool: Tinkercad

Code Description:
Pins 12, 11, 10, 9, and 8 are stored in the array ledPins.
Pin A0 is used to read the potentiometer value.
In setup(), a while loop sets all LED pins as OUTPUT.
In loop():
Read potentiometer value using analogRead().
Map the value to a PWM range (0–255) with map().
Turn LEDs ON one by one, gradually increasing brightness to the mapped value.
Turn LEDs OFF one by one, gradually decreasing brightness to 0.
Delays are added to create a smooth running light effect.

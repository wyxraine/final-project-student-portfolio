Laboratory Activity #1: Working with Digital Signals

Objectives:
1. Review Arduino as a device for IoT systems implementation.
2. Discuss digital signals and their implementation in an Arduino circuit.

Activity Description:
This laboratory activity focuses on creating a running light circuit using an Arduino board.
LEDs connected to digital pins 8 to 12 are programmed to turn on one by one from pin 12 down to pin 8, then turn off in the same sequence. 
A 1-second delay is applied between each LED transition. The activity demonstrates the use of digitalWrite() for controlling digital output signals in an Arduino circuit.

Expected Output:
The LEDs light up sequentially from pin 12 to pin 8, then turn off sequentially from pin 12 to pin 8, repeating continuously with a 1-second delay.

Tools and Components Used:
* Hardware: Arduino Uno, LEDs, Breadboard, Jumper Wires, Resistors
* Software: Arduino IDE
* Diagram Tool: Tinkercad

Code Description:
The Arduino pins 12, 11, 10, 9, and 8 are stored in an array called ledPins.
In the setup() function, all pins in the array are set as OUTPUT using a for-loop.
In the loop() function:
The first for-loop turns ON each LED in sequence, waiting 1 second (delay(1000)) between each.
The second for-loop turns OFF each LED in sequence, also waiting 1 second between each.
This cycle repeats continuously, creating a running light effect.


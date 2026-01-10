Laboratory Activity #6: Bidirectional Control Using Arduino and Python

Members: Andino Llantos Gomba Ochoa Palomar

Objectives:
* Understand and implement Arduino Serial Connection.
* Utilize Python as a tool for implementing serial communication.
* Create a simple circuit that implements bidirectional communication between Arduino and Python.

Activity Description:
This laboratory activity involves creating a bidirectional communication system between an Arduino and a Python program using serial connection. 
Three push buttons are connected to the Arduino to send outbound signals to Python, while three LEDs are controlled through inbound signals received from Python. When a button is pressed, the Arduino sends a character ('R', 'G', or 'B') to Python. The Python program then responds by sending back a command ('1', '2', or '3'), which instructs the Arduino to toggle the corresponding LED. 
This setup demonstrates real-time two-way communication between hardware and software.

Expected Output:
When Button 1 is pressed, Arduino sends 'R' and Python replies with '1', toggling the red LED.
When Button 2 is pressed, Arduino sends 'G' and Python replies with '2', toggling the green LED.
When Button 3 is pressed, Arduino sends 'B' and Python replies with '3', toggling the blue LED.
All responses occur in less than one second.

Tools and Components Used:
* Hardware: Arduino Uno, 3 LEDs (Red, Green, Blue), 3 Push Buttons, Breadboard, Jumper Wires, Resistors
* Software: Arduino IDE, Python, PySerial Library
* Diagram Tool: Tinkercad

Code Description:

Arduiono File: bidirectional_control.ino
Contains the Arduino program for this activity. It sets the pins for the three LEDs and three push buttons. 
The Arduino reads the button presses and sends a single character ('R', 'G', or 'B') through the Serial port when a button is pressed.
It also listens for incoming Serial data from the Python program. 
When it receives '1', '2', or '3', it toggles the red, green, or blue LED. 
This file handles all hardware input and output operations.

Python file: bidirectional_control.py
Contains the Python program used for serial communication with the Arduino. 
It opens the serial port and continuously listens for characters sent by the Arduino.
When it receives 'R', 'G', or 'B', it sends back '1', '2', or '3' to the Arduino. 
This file handles the computer-side control and ensures real-time bidirectional communication between Python and Arduino.

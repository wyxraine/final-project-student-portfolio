Laboratory Activity #7: Controlling Arduino using FastAPI

Members:
Andino
Llantos
Gomba
Ochoa
Palomar

Objectives:
* Understand and implement Arduino Serial Connection
* Utilize Python as a tool for implementing serial connection, and implement a HTTP-based solution using FastAPI
* Create a simple circuit what will implement bi-directional connection between Arduino and Python using FastAPI

Activity Description:
This laboratory activity involves creating a bidirectional communication system between an Arduino and a Python FastAPI web application using serial connection.
Three push buttons are connected to the Arduino to send outbound signals, while three LEDs are controlled through inbound signals received from the FastAPI server.
When a button is pressed, the Arduino toggles the corresponding LED and sends a status message through the Serial port.
When a web API endpoint is accessed, the FastAPI program sends a command character ('1', '2', or '3') to the Arduino, which instructs it to toggle the corresponding LED.
This setup demonstrates real-time two-way communication between hardware and a web-based software interface.

Expected Output:
When Button 1 is pressed, the red LED toggles and Arduino prints "BUTTON: RED TOGGLED" on the Serial Monitor.
When Button 2 is pressed, the green LED toggles and Arduino prints "BUTTON: GREEN TOGGLED".
When Button 3 is pressed, the blue LED toggles and Arduino prints "BUTTON: BLUE TOGGLED".
When the FastAPI endpoint /led/red is accessed, the FastAPI server sends '1' and the Arduino toggles the red LED.
When the FastAPI endpoint /led/green is accessed, the FastAPI server sends '2' and the Arduino toggles the green LED.
When the FastAPI endpoint /led/blue is accessed, the FastAPI server sends '3' and the Arduino toggles the blue LED.
All responses occur in less than one second.

Tools and Components Used:
* Hardware: Arduino Uno, 3 LEDs (Red, Green, Blue), 3 Push Buttons, Breadboard, Jumper Wires, Resistors
* Software: Arduino IDE, Python, FastAPI Framework, PySerial Library
* Diagram Tool: Tinkercad

Code Description:
Arduino File: arduino_control.ino
Contains the Arduino program for this activity. It sets the pins for the three LEDs and three push buttons.
The Arduino reads the button presses and toggles the corresponding LED while sending status messages through the Serial port.
It also listens for incoming Serial data from the FastAPI program.
When it receives '1', '2', or '3', it toggles the red, green, or blue LED.
It also accepts 'O' and 'F' commands to turn all LEDs ON or OFF.
This file handles all hardware input and output operations.

Python File: arduino_control.py
Contains the Python program used for serial communication between the FastAPI server and Arduino.
It opens the serial port and defines web API endpoints for LED control.
When an endpoint is accessed, it sends command characters ('1', '2', '3', 'O', 'F') to the Arduino through serial communication.
This file handles the web-based computer-side control and ensures real-time bidirectional communication between the FastAPI server and Arduino.

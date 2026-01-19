Laboratory Finals Examination

Members:
Andino
Llantos
Gomba
Ochoa 
Palomar

Tools and Components Used:
* Hardware: Arduino Uno, Push Button, Breadboard, Jumper Wires, Resistors
* Software: Arduino IDE, Python, PySerial Library, Requests Library, FastAPI Web Server

Code Description:

Arduino File: final_exam_button_sender.ino
Contains the Arduino program for the laboratory final examination.
It sets the pin connection for a push button using the internal pull-up resistor.
The Arduino continuously monitors the button state. When the button is pressed, the program applies a debounce delay to ensure accurate detection. After validation, the Arduino sends a predefined group number through the Serial port.
This file handles button input detection, debounce processing, and serial data transmission to the computer-side program.

Python File: final_exam_serial_to_api.py
Contains the Python program used for serial communication and web API interaction.
It opens the serial port to receive data sent by the Arduino. 
When a valid group number is received, the program constructs a corresponding API endpoint and sends an HTTP GET request to a FastAPI web server.
The Python program also displays status messages indicating successful API calls.
This file handles computer-side serial data reception, API request processing, and real-time communication between the Arduino hardware and the web-based system.

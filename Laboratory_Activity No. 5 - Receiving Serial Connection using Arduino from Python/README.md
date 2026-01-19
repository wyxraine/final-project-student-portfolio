Laboratory Activity #5: Receiving Serial Connection using Arduino from Python

Members:
Andino
Llantos
Gomba
Ochoa
Palomar

Objectives
* Understand and implement Arduino Serial Connection.
* Utilize Python as a tool for implementing serial communication.
* Create a simple circuit that can be controlled using Serial connection between Arduino and Python.

Activity Description:
This laboratory activity involves creating an Arduino LED control system that communicates with a Python program via the serial port.
The Arduino board controls three LEDs (Red, Green, Yellow) connected to digital pins 8, 9, and 10.
The Python program provides a menu interface where users can toggle individual LEDs, turn all LEDs on/off, or exit the program.
Commands sent from Python are received and executed by the Arduino, which responds with confirmation messages.

Expected Output:
Users can turn on/off individual LEDs by selecting the corresponding option in the Python menu.
Users can also turn all LEDs on or off at once.
The Arduino sends back a message confirming the action taken.
The program continuously waits for user input until the exit command is chosen.

Tools and Components Used:
* Hardware: Arduino Uno, Red LED, Green LED, Yellow LED, Breadboard, Jumper Wires, Resistors
* Software: Arduino IDE, Python 3
* Diagram Tool: Tinkercad 

Code Description:

Python File: (Led_Control.py)
Establishes serial communication with Arduino using pyserial.
Displays a menu with options: Red ON/OFF, Green ON/OFF, Yellow ON/OFF, All ON, All OFF, Exit.
Sends the corresponding command to the Arduino based on user input.
Reads and displays Arduino’s responses in real-time.

Arduino File: (LedFunctions.h + lab_1_finals.ino)
LedFunctions.h contains functions to initialize LEDs, toggle individual LEDs, turn all LEDs on/off, and apply LED states.
Pin definitions: Red → 8, Green → 9, Yellow → 10.
Boolean variables track the current state of each LED.
setup() initializes LED pins and starts serial communication.
loop() continuously checks for incoming serial commands and executes the corresponding LED function.
Commands are case-insensitive and confirmed via Serial messages.

Laboratory Midterm Examination

Members:
Andino
Llantos
Gomba
Ochoa
Palomar

Tools and Components Used:
Hardware: Arduino Uno, Photoresistor, 3 LEDs (Green, Yellow, Red), Breadboard, Jumper Wires, Resistors
Software: Arduino IDE, Serial Monitor

Code Description:

Arduino File: MIDTERM_IOT.ino
Contains the Arduino program for the laboratory midterm examination.
It sets the pin connections for the photoresistor sensor and three LEDs (Green, Yellow, Red).
The Arduino continuously reads the analog value from the photoresistor and converts it into a light intensity percentage. B
ased on the measured intensity, the system controls LED outputs in two operating modes: MANUAL and AUTO.

In MANUAL mode, the LEDs are controlled using user-defined threshold values. 
The user can send Serial commands such as SET LOW xx and SET HIGH xx to adjust the low and high threshold limits. The Arduino then updates the LED indicators based on these thresholds.
In AUTO mode, the system automatically determines the environment condition as Cloudy, Normal, or Bright Sunlight based on the light intensity. 
Each environment condition corresponds to a specific LED indicator.

The program also listens for Serial commands to switch modes:
MODE AUTO switches to automatic mode
MODE MANUAL switches to manual mode

The Arduino prints real-time sensor readings, LED status, current mode, and environment condition to the Serial Monitor.

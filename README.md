**SMART RATION MONITERING AND STOCK MONITERING SYSTEM**

**1\. Aim**

To develop a smart ration dispensing prototype that uses RFID-based user identification and servo-controlled dispensing mechanisms to automate the distribution of different ration materials.  
**2\. Problem Statement**

Traditional ration distribution requires manual handling and measurement of materials. This can lead to delays, incorrect quantities, and difficulty in maintaining an organized dispensing process.  
The proposed system aims to automate the dispensing process using an RFID-based identification system and separate servo-controlled compartments for different ration materials.  
**3\. Objectives**

To identify authorized users using an RFID card.  
To control three separate dispensing mechanisms using servo motors.  
To provide separate compartments for different ration materials.  
To display system information using an LCD.  
To explore Wi-Fi connectivity using the ESP-01 module.  
To develop a compact working prototype for automated ration distribution.  
4\. Proposed Solution  
The system consists of three separate ration compartments. Each compartment is operated by an individual servo motor.  
When an authorized RFID card is detected, the Arduino processes the card information and activates the corresponding dispensing mechanism. The LCD can be used to display the current operation or user information.  
The ESP-01 module is integrated to provide Wi-Fi communication for future monitoring and data-management features.  
**5\. Components Required**

5 V power supply  
DC-DC buck converter  
External Ration storage/dispensing compartmentsArduino board  
RFID RC522 module  
RFID card/tag  
3 × Servo motors  
16×2 I2C LCD  
ESP-01 Wi-Fi module  
Breadboard  
Jumper wires  
6\. Hardware Setup  
The prototype was physically assembled using three separate compartments. A servo motor was mounted on each compartment to control its dispensing mechanism.  
The Arduino was used as the main controller, while the LCD was mounted on the prototype to provide a visual display.  
The servo motors were connected separately so that each ration compartment could be controlled independently.  
**7\. Pin Configuration**

Component  
Arduino Pin  
Rice Servo  
D9  
Wheat Servo  
D10  
Sugar Servo  
D11  
Buzzer  
D7  
RFID SS/SDA  
D53  
RFID RST  
D49  
RFID SCK  
D52  
RFID MOSI  
D51  
RFID MISO  
D50  
LCD SDA  
D20  
LCD SCL  
D21  
ESP-01 TX  
RX1 / D19  
ESP-01 RX  
TX1 / D18  
The three servo signals are configured on D9, D10 and D11 in the project design. �  
Smart\_Ration\_System.docx  
**8\. Working Principle**

The system is powered on.  
The Arduino initializes the connected modules.  
The user places an RFID card near the RFID reader.  
The RFID module reads the card UID.  
The Arduino checks whether the card is authorized.  
After successful identification, the required servo motor is activated.  
The servo opens the corresponding dispensing mechanism.  
The ration material is released through the respective compartment

The servo returns to its initial position.  
The LCD provides information about the current system operation.  
**9\. Servo Motor Control**

Three servo motors were mounted on the three ration compartments.  
Servo 1 → Rice  
Servo 2 → Wheat  
Servo 3 → Sugar  
Each servo is controlled independently by the Arduino. This allows the three ration materials to have separate dispensing mechanisms.  
10\. RFID Integration  
The RFID module is used for user identification.  
The RFID reader detects the card and provides its UID to the Arduino. The controller compares the detected UID with the authorized UID stored in the program.  
This provides a basic authentication mechanism before dispensing.  
**11\. LCD Display**

A 16×2 I2C LCD was integrated into the prototype.  
It can be used to display messages such as:  
Scan Your Card  
Card Accepted  
Dispensing...  
Thank You  
**12\. ESP-01 Wi-Fi Integration**

The ESP-01 module was connected to the Arduino to provide Wi-Fi communication.  
The module was tested using AT commands and successfully connected to a Wi-Fi network during the development process. �  
Smart\_Ration\_System.docx  
This provides a foundation for future features such as:  
Online stock monitoring  
User transaction records  
Remote monitoring  
Cloud data upload  
**13\. Testing and Verification**

During today's development, the following were tested:  
RFID card detection  
Individual servo motor control  
Three-servo integration  
LCD connection  
ESP-01 Wi-Fi connectivity  
Power connections  
Physical mounting of the dispensing mechanisms  
Overall prototype integration  
The servo motors were also tested individually to verify their movement before integrating them into the complete dispensing system.  
**14\. Advantages**

Reduces manual dispensing work.  
Provides RFID-based identification.  
Allows separate control of multiple ration compartments.  
Provides a simple LCD interface.  
Can be extended with IoT functionality.  
Suitable for further automation and monitoring.  
**15\. Limitations**

The current prototype does not yet use a load cell for accurate weight measurement.  
The dispensing quantity is not automatically measured by weight.  
The current prototype requires further mechanical refinement.  
The Wi-Fi section can be expanded for complete online monitoring.  
**16\. Future Scope**

Future improvements can include:  
Load-cell-based quantity measurement  
Automatic quantity control  
Online stock-level monitoring  
Cloud database integration  
Mobile/web application  
Transaction history  
Low-stock alerts  
Multiple-user management  
Automatic inventory calculation  
**17\. Result**

A working prototype of the Smart Ration Dispensing System was assembled with three separate ration compartments and three servo-controlled dispensing mechanisms. RFID identification, LCD interfacing, and ESP-01 Wi-Fi connectivity were also integrated/tested as part of the system development.  
**18\. Project Images**

Add today's prototype image under this section:  
Prototype – Three-Compartment Smart Ration Dispensing System  
**19\. Conclusion**

The prototype demonstrates how RFID, servo motors, LCD, Arduino, and Wi-Fi communication can be combined to create an automated ration dispensing system. Today's work mainly focused on building the physical prototype, integrating the three dispensing mechanisms, and testing the individual hardware modules. The system can be further developed by adding load-cell-based measurement and complete IoT monitoring.  
**20.Project image** 
This schematic shows the complete I²C based temperature sensing circuit using the LM92CIMX/NOPB digital temperature sensore powered from 3.3V. The LM92 receives power through Pin 8 (VS+), which is tied to the 3.3V rail and separated with a 0.1 uF capacitor (C5) placed between VS+ and ground for noise reduction and stable operation. Pin 4 (GND) connects directly to system ground. Communication with the microcontroller is provided through the SDA (pin 1) and SCL (pin 2) lines, which follow the I²C protocol. The LM92 uses open drain outputs, each line is pulled up to 3.3V using 10K resistors (R1 and R2) to ensure proper behavior. Which these lines connect to the system I²C bus. The device address is configured using the address select pins A0 (pin 7) and A1 (pin 6). Both pins are tied to the ground, selecting the lowest I²C address for the sensor. The T_CRIT_A (pin 3) alarm output is not used in this design and the INT (pin 5). This schematic provides a standard and stable I²C temperature sensing subsystem. This is a Test to see if it updates.

<img width="1022" height="626" alt="Screenshot 2025-11-29 194248" src="https://github.com/user-attachments/assets/3029044c-0244-4307-887e-9a8adec4c345" />

## PCB Pictures 

**Font**
![Fall 25 PCB Team Board Front](https://github.com/user-attachments/assets/f80bbc3a-84eb-448c-8539-e3882310d657)


**Back**
![Fall 25 PCB Team Board Back](https://github.com/user-attachments/assets/504e50a7-bf09-48a2-9e4c-65a5a37bf2c6)






[Bryant_Sophie_Temp_Sensor_S25.pdf](https://github.com/user-attachments/files/20051428/Bryant_Sophie_Temp_Sensor_S25.pdf)




[Bryant_Sophie_Temp_S25.zip](https://github.com/user-attachments/files/20051434/Bryant_Sophie_Temp_S25.zip)






[Gerber_Temp_S25_P2.zip](https://github.com/user-attachments/files/20051437/Gerber_Temp_S25_P2.zip)

## Team Final PCB Photos

**Font**
![Fall 25 PCB Team Board Front](https://github.com/user-attachments/assets/86486cbf-39f9-4b06-8caf-08609513aa1e)


**Back**
![Fall 25 PCB Team Board Back](https://github.com/user-attachments/assets/43d77a7a-b0ef-43d4-bd60-6be863b24d8d)


## Functionality 
This PCB is a custom microcontroller development board designed for an EGR 314 embedded-systems project. At the center is the main controller footpaint, which connects to various programming headers, and test points. The left side includes supporting circuitry such as a sensor or secondary I²C, a switch, and a passive components needed for conditioning signals. The bottom section contains the power-input stage with a fuse, filtering capacitors, and connectors to safely regulate and distribute power. On the right side, multiples LEDs that help provide visual feedback for debugging digital outputs, while the I²C is the power driver. Overall, the board integrates processing, power regulation, user interface, debugging points, and expansion connectors to support the micocontroller programming and hardware testing.

## Team Design/Decision Making
We orignially wanted to extend this design for our robotic arm, additional components such as motors, a motor driver, and an ESP32 module were suppose to be provided by teammates. The PIC microcontroller can be programmed to control motor drivers through digital signals while monitoring temperature data from the temp sensor via I²C. The existing UART daisy chain headers provide a convenient interface for connecting the ESP32, which enables wireless communication through Wi-Fi. In this configuration, the ESP32 can issue control commands to the PIC or directly interface with the motor driver for real-time motion control. The 9V power supply used in the subsystem can also be utilized to power the motor driver, provided appropriate voltage regulation and current capacity are ensured. With these enhancements, the subsystem becomes capable of wirelessly controlled robotic motion while monitoring the temperature to prevent overheating or system failure.

## How can it improve
For the temperature PCB, more spacing could be improved to make it easier to solder. Adding a motor control, wireless communication, and power management would help improve it as well. First, a motor driver should be added to control motors, with digital signals provided from the microcontroller pins. The motors would enable movement of the robotic arm’s joints while ensuring safe motor operation through the use of protective components. Additionally, integrating an ESP32 module would introduce wireless control via Wi-Fi, connected through UART or I²C for communication with the PIC microcontroller. To help the higher current of motors, a dedicated 5V regulator should be included to power the motors independently from the 3.3V, helping to prevent voltage drops and system instability. It is also recommended to incorporate system feedback components such as limit switches, encoders to improve control precision and ensure safe operation. The temperature sensor can be utilized to implement temperature protection by disabling motors if the temperature overheats. These would help collectively transform the current subsystem into a robust and responsive platform capable of driving and monitoring a functional robotic arm.

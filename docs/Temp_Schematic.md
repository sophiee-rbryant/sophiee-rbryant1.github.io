This schematic shows the complete I2C based temperature sensing circuit using the LM92CIMX/NOPB digital temperature sensore powered from 3.3V. The LM92 receives power through Pin 8 (VS+), which is tied to the 3.3V rail and separated with a 0.1 uF capacitor (C5) placed between VS+ and ground for noise reduction and stable operation. Pin 4 (GND) connects directly to system ground. Communication with the microcontroller is provided through the SDA (pin 1) and SCL (pin 2) lines, which follow the I2C protocol. The LM92 uses open drain outputs, each line is pulled up to 3.3V using 10K resistors (R1 and R2) to ensure proper behavior. Which these lines connect to the system I2C bus. The device address is configured using the address select pins A0 (pin 7) and A1 (pin 6). Both pins are tied to the ground, selecting the lowest I2C address for the sensor. The T_CRIT_A (pin 3) alarm output is not used in this design and the INT (pin 5). This schematic provides a standard and stable I2C temperature sensing subsystem. 

<img width="1022" height="626" alt="Screenshot 2025-11-29 194248" src="https://github.com/user-attachments/assets/3029044c-0244-4307-887e-9a8adec4c345" />

## PCB Pictures 

**Font**
![download (2)](https://github.com/user-attachments/assets/710c47b2-65c3-4bf9-9085-83be407c3cd2)

**Back**
![download (3)](https://github.com/user-attachments/assets/be8da0cb-387d-44aa-8e76-6fa1f9bad142)





[Bryant_Sophie_Temp_Sensor_S25.pdf](https://github.com/user-attachments/files/20051428/Bryant_Sophie_Temp_Sensor_S25.pdf)




[Bryant_Sophie_Temp_S25.zip](https://github.com/user-attachments/files/20051434/Bryant_Sophie_Temp_S25.zip)






[Gerber_Temp_S25_P2.zip](https://github.com/user-attachments/files/20051437/Gerber_Temp_S25_P2.zip)

## Team Final PCB Photos

**Font**
![download (2)](https://github.com/user-attachments/assets/710c47b2-65c3-4bf9-9085-83be407c3cd2)

**Back**
![download (3)](https://github.com/user-attachments/assets/be8da0cb-387d-44aa-8e76-6fa1f9bad142)

## Functionality 
This schematic represents a complete temperature sensing subsystem designed to operate using a 9V external adapter. The system powers a PIC18F47Q10 microcontroller, communicates with the temperature sensor via I²C, provides UART daisy chaining, and includes a reset circuit, programming interface, and multiple debugging LEDs for monitoring functionality.

## Team Design/Decision Making
We orignially wanted to extend this design for our robotic arm, additional components such as motors, a motor driver, and an ESP32 module were suppose to be provided by teammates. The PIC microcontroller can be programmed to control motor drivers through digital signals while monitoring temperature data from the temp sensor via I²C. The existing UART daisy chain headers provide a convenient interface for connecting the ESP32, which enables wireless communication through Wi-Fi. In this configuration, the ESP32 can issue control commands to the PIC or directly interface with the motor driver for real-time motion control. The 9V power supply used in the subsystem can also be utilized to power the motor driver, provided appropriate voltage regulation and current capacity are ensured. With these enhancements, the subsystem becomes capable of wirelessly controlled robotic motion while monitoring the temperature to prevent overheating or system failure.

## How can it improve
For the temperature PCB, more spacing could be improved to make it easier to solder. Adding a motor control, wireless communication, and power management would help improve it as well. First, a motor driver should be added to control motors, with digital signals provided from the microcontroller pins. The motors would enable movement of the robotic arm’s joints while ensuring safe motor operation through the use of protective components. Additionally, integrating an ESP32 module would introduce wireless control via Wi-Fi, connected through UART or I²C for communication with the PIC microcontroller. To help the higher current of motors, a dedicated 5V regulator should be included to power the motors independently from the 3.3V, helping to prevent voltage drops and system instability. It is also recommended to incorporate system feedback components such as limit switches, encoders to improve control precision and ensure safe operation. The temperature sensor can be utilized to implement temperature protection by disabling motors if the temperature overheats. These would help collectively transform the current subsystem into a robust and responsive platform capable of driving and monitoring a functional robotic arm.

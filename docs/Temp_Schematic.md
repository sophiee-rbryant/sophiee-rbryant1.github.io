The schematic of the temperature sensor includes a voltage regulator of 3.3V that is required by the PIC Microship. It will help to keep the temperature connected and the PIC is shows with pins are connected to the temperature sensor.

![Screenshot 2025-04-27 153625](https://github.com/user-attachments/assets/d00ffe5a-0efc-4fa5-a905-deb4958b80fd)

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

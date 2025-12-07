This schematic shows the complete I²C based temperature sensing circuit using the LM92CIMX/NOPB digital temperature sensore powered from 3.3V. The LM92 receives power through Pin 8 (VS+), which is tied to the 3.3V rail and separated with a 0.1 uF capacitor (C5) placed between VS+ and ground for noise reduction and stable operation. Pin 4 (GND) connects directly to system ground. Communication with the microcontroller is provided through the SDA (pin 1) and SCL (pin 2) lines, which follow the I²C protocol. The LM92 uses open drain outputs, each line is pulled up to 3.3V using 10K resistors (R1 and R2) to ensure proper behavior. Which these lines connect to the system I²C bus. The device address is configured using the address select pins A0 (pin 7) and A1 (pin 6). Both pins are tied to the ground, selecting the lowest I²C address for the sensor. The T_CRIT_A (pin 3) alarm output is not used in this design and the INT (pin 5). This schematic provides a standard and stable I²C temperature sensing subsystem. This is a Test to see if it updates.

<img width="1022" height="626" alt="Screenshot 2025-11-29 194248" src="https://github.com/user-attachments/assets/3029044c-0244-4307-887e-9a8adec4c345" />

<hr style="border: 1px solid #E91E63;">

## <span style="color:#E91E63; font-weight:700;">PCB Pictures</span>

## <span style="color:#E91E63; font-weight:700;">Front</span>
![Fall 25 PCB Team Board Front](https://github.com/user-attachments/assets/f80bbc3a-84eb-448c-8539-e3882310d657)


### <span style="color:#E91E63; font-weight:700;">Back</span>
![Fall 25 PCB Team Board Back](https://github.com/user-attachments/assets/504e50a7-bf09-48a2-9e4c-65a5a37bf2c6)






[Bryant_Sophie_Temp_Sensor_S25.pdf](https://github.com/user-attachments/files/20051428/Bryant_Sophie_Temp_Sensor_S25.pdf)




[Bryant_Sophie_Temp_S25.zip](https://github.com/user-attachments/files/20051434/Bryant_Sophie_Temp_S25.zip)






[Gerber_Temp_S25_P2.zip](https://github.com/user-attachments/files/20051437/Gerber_Temp_S25_P2.zip)

<hr style="border: 1px solid #E91E63;">

### <span style="color:#E91E63; font-weight:700;">Functionality</span>

The functionality of this schematic meets our user needs and product requirements by ensuring that every subsystem works together to collect reliable environmental data. The voltage regulator provides a stable 3.3-volt supply, which keeps all components powered safely and prevents system resets during outdoor temperature swings. The ESP32 microcontroller serves as the core of the device and manages all communication, allowing sensors to report data consistently. The pressure sensor and temperature sensor each connect through properly designed signal paths, enabling accurate measurements of weather conditions such as temperature, humidity, and atmospheric changes. The shift register and LEDs provide visual indicators, giving users quick feedback during testing and deployment. Test points and jumpers make the device easier to debug, repair, and maintain. Together, these circuit functions support long-term monitoring, early wildfire detection, and reliable operation in remote environments.


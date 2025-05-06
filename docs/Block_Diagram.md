Block Diagram of the Subsystem: Temperature Sensor

The temperature sensor chosen in our project will be LM92CIMX/NOPB from Texas Instruments. It will ensure thermal management and safe operation by shutting down the system if the temerature exceeds safe thresholds. This will help protect the project from thermal runaway or any fire hazards, also detect any component failure that can be caused by abnormal temperature spikes.

![Screenshot 2025-05-05 165558](https://github.com/user-attachments/assets/f44b6ce0-fd7e-4632-9979-0952f819492d)


**Feedback**
*
Adding more LEDs to help with reading and to ensure everything works properly
*
Adding a Microchip snap programmer with supoorting the PIC18F47Q10. Using MPLAB supports it as well and helps with debugging
*
9V 3A wall power supply and a barrel jack helps the Temp sensor by indirectly providing it with the regulated voltage it needs to operate

**Decision Making Process**
I made significant adjustments to my subsystem design after conducting peer reviews and reviewing the standard project requirements. It helped me identify key areas for improvement, particularly in power management, communication interfaces, and debugging capabilities. To enhance the system’s reliability and compatibility, I included a 9V wall adapter as the main power source. This input voltage is regulated down to 3.3V using a switching voltage regulator to power the temperature sensor and microcontroller. Connecting the LM92 temperature sensor to the PIC18F47Q10 microcontroller using the I²C protocol, helping to provide accurate and consistent data transmission. Additionally, I added more of the debugging LEDs on the board. Not only did it help provide real-time visual feedback during testing and troubleshooting but it also gave me the flexibility to incorporate additional indicators for future system enhancements. These modifications collectively improved the overall functionality, maintainability, and adaptability of my subsystem.

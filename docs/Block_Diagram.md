<img width="1354" height="1248" alt="image" src="https://github.com/user-attachments/assets/ca81645f-36e9-49a5-8389-7dc787cb8b7e" />

[PDF of Block Diagram](https://github.com/user-attachments/files/23953043/Team313_BlockDiagramV2.pdf)

<hr style="border: 1px solid #E91E63;">

## <span style="color:#E91E63; font-weight:700;">Decision Making Process of the Block Diagram</span>

We structured the block diagram by first mapping our core product requirements into subsystems: power, sensing, processing, communication, and indication. From there we placed the ESP32-S3-WROOM-1-N4 at the center because it is responsible for all decisions, data processing, and wireless communication. The 9 V battery and LM2575D2T-3.3R4G regulator were placed on the left as the single power path so it is clear that every other block ultimately depends on a regulated 3.3 V rail. The BME280 pressure/temperature/humidity sensor and LM92 temperature sensor are shown on I²C links into the ESP32 to emphasize that all environmental data flows through a common digital bus. On the right, the 74HC595PW shift register and LED block are connected by SPI / digital-parallel lines to show how the microcontroller expands its outputs to drive multiple visual indicators. Finally, the ESP-NOW cloud in the center-top shows that the same ESP32 both transmits and receives data, tying the remote node into a wider network of wildfire-monitoring stations. This structure directly reflects the product requirements: stable off-grid power, multi-sensor environmental monitoring, wireless early-warning communication, and clear visual feedback for local users.

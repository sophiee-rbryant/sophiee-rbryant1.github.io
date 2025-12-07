| <span style="color:#E91E63;">Solution</span> | <span style="color:#E91E63;">Pros</span> | <span style="color:#E91E63;">Cons</span> |
| -------- | ---- | ---- |
| ![Screenshot 2025-03-02 154251](https://github.com/user-attachments/assets/5a53ca9e-b34c-42ca-988b-d36ee0cbb177) [Link to Product](https://www.digikey.com/en/products/detail/silicon-labs/SI7055-A20-IMR/5023917) | ![Screenshot 2025-03-02 154424](https://github.com/user-attachments/assets/d154704d-83ee-42de-9dba-d0ae9cea7d9b) | ![Screenshot 2025-03-02 154459](https://github.com/user-attachments/assets/b809e7a3-f78b-47cc-8131-a51a5b655fdf) |
| ![Screenshot 2025-03-02 154556](https://github.com/user-attachments/assets/c3d631d6-c5f0-43db-b305-7b91b05f1304) [Link to Product](https://www.digikey.com/en/products/detail/texas-instruments/LM92CIMX-NOPB/367372) | ![Screenshot 2025-03-02 155527](https://github.com/user-attachments/assets/0ac3c732-26b0-471a-887a-78ff86a80186) | ![Screenshot 2025-03-02 155544](https://github.com/user-attachments/assets/72dda075-4710-4ad2-80e7-979abffc87b5) |
| ![Screenshot 2025-03-02 154959](https://github.com/user-attachments/assets/56dd8b9b-2493-49e9-8d66-b7593e9ce6fd) [Link to Product](https://www.digikey.com/en/products/detail/analog-devices-inc/ADT7410TRZ-REEL7/2056653) | ![Screenshot 2025-03-02 155043](https://github.com/user-attachments/assets/fea8fab4-4c5e-4898-8ae8-6d3336f1967d) | ![Screenshot 2025-03-02 155117](https://github.com/user-attachments/assets/af6878ae-8a4b-4752-86bf-60766b06cd9a) |

![Screenshot 2025-03-02 160459](https://github.com/user-attachments/assets/c3b2775b-207e-4f34-a677-c62403ee0de6)



<hr style="border: 1px solid #E91E63;">

## <span style="color:#E91E63; font-weight:700;">Bill of Materials</span>

<img width="2363" height="1220" alt="image" src="https://github.com/user-attachments/assets/20bcba65-6862-4ace-ba67-2847cfd92582" />

[Team 313 Bill of Materials.xlsx - Sheet1.pdf](https://github.com/user-attachments/files/22654392/Team.313.Bill.of.Materials.xlsx.-.Sheet1.pdf)


We used the power budget to estimate our system’s total current draw by listing every active component, pulling its maximum current from the datasheet, and multiplying it by the quantity shown in the BOM. By assuming worst-case conditions, ESP32 transmitting, all sensors active, and all LEDs on. We created a conservative estimate rather than relying on typical values. After summing all currents and adding design margin, we compared the total to the LM2575D2T-3.3R4G regulator’s 1 A limit.

The analysis showed that our system remains well below the regulator’s maximum output, meaning the 3.3 V rail is stable, safe, and capable of supporting all components without risk of brownout. This confirms that our chosen regulator and input supply provide enough headroom for reliable operation and small future expansions.

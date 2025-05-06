---
title: API
---

 ## Message Tables

 
**Safety Message Sent to Motor**


| Field         | Value                                                   |
|---------------|---------------------------------------------------------|
| Byte 1        | msg_type                                                |
| Variable Type | uint8_t                                                 |
| Min Value     | 0                                                       |
| Max Value     | 1                                                       |
| Use           | To make sure the temperature on motor does not overheat |


**Message to LED**


| Field         | Value                |
| ------------- | -------------------- |
| Byte 1        | LED_set              |
| Variable Type | uint8_t              |
| Min Value     | 0                    |
| Max Value     | 1                    |
| Use           | To show it is in use |


## Team UML
![Screenshot 2025-05-05 155907](https://github.com/user-attachments/assets/471b7be5-e13f-4b95-80c2-1caec39096c8)

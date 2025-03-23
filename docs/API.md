---
title: API
---

| Message Type Byte 1 - 2 (uint16_t) | Description |
| ---- | ---- |
| 2 | User Safe |
| 7 | Temperature |


## Message Type 2: User Safe
|  | Byte 3 |
| ---- | ---- |
| Var Name | user |
| Var Type | uint16_t |
| Min Val | 0 |
| Max Val | 1 |
| Example | 1 |


## Message Type 7: Temperature
|  | Byte 4 |
| ---- | ---- |
| Var Name | temp |
| Var Type | uint16_t |
| Min Val | 0 |
| Max Val | 1 |
| Example | 1 |

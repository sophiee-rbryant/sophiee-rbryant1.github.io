---
title: Message Structure
---

## Message Type - User Safe
| | Byte 1 | Byte 2 |
| --- | ---- | ---- |
| Variable Name | Read Temperature | User Safe |
| Variable Type | 7 | Temperature |
| Min | 0 | 1 |
| Max | 1 | 7 |
| Use | To read temperature from product | Tells the system to shut down the product |

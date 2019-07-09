---
layout: post
title:  "Supported Hardware"
permalink: /hardware/
---

Supported Hardware
==================
The Hardware supported are:
  * NXP VF610 (Cortex-M4 only)
  * NXP IMX6sx (Cortex-M4 only)
  * NXP S32k
  * ST STM32
  * TI AM57xx (Cortex-M4 only)

Driver Support for each core:

| Platform | GPIO | UART | SPI | Timer | PWM | Capture | SD | Net | CAN | Mailbox | Remoteproc |
|----------|:----:|:----:|:---:|:-----:|:---:|:-------:|:--:|:---:|:---:|:-------:|:----------:|
| VF610    |  x   |  x   |  x  |   x   |  x  |    x    | -  |  -  |  -  |    -    |      -     |
| IMX6sx   |  x   |  x   |  -  |   x   |  x  |    x    | -  |  x  |  -  |    x    |      x     |
| S32k     |  x   |  x   |  -  |   x   |  x  |    x    | -  |  /  |  -  |    -    |      -     |
| STM32    |  x   |  x   |  x  |   x   |  x  |    x    | x  |  -  |  -  |    -    |      -     |
| AM57xx   |  x   |  x   |  x  |   x   |  x  |    x    | -  |  -  |  -  |    -    |      -     |


x=supported, /=not testet, o=only software emulation supported

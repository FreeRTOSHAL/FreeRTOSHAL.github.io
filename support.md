---
layout: post
title:  "Supported Hardware"
permalink: /hardware/
---

The Hardware supported are:
  * NXP VF610 (Cortex-M4 only)
  * NXP IMX6sx (Cortex-M4 only)
  * NXP S32k
  * ST STM32
  * TI AM57xx (Cortex-M4 only)
  * TI TMS320C28x (TI DSP)

Driver Support for each core:

| Platform   | GPIO | UART | ADC | SPI | Timer | PWM | Capture | SD | Net | CAN | Mailbox | Remoteproc | Temp  | 
|------------|:----:|:----:|:---:|:---:|:-----:|:---:|:-------:|:--:|:---:|:---:|:-------:|:----------:|:-----:|
| VF610      |  x   |  x   |  x  |  x  |   x   |  x  |    x    | -  |  -  |  /  |    -    |      -     |   -   |
| IMX6sx     |  x   |  x   |  -  |  -  |   x   |  x  |    x    | -  |  x  |  /  |    x    |      x     |   -   |
| S32k       |  x   |  x   |  -  |  -  |   x   |  x  |    x    | -  |  /  |  x  |    -    |      -     |   -   |
| STM32      |  x   |  x   |  x  |  x  |   x   |  x  |    x    | x  |  -  |  -  |    -    |      -     |   -   |
| AM57xx     |  x   |  x   |  -  |  x  |   x   |  x  |    x    | -  |  -  |  x  |    x    |      x     |   x   |
| TMS320C28x |  x   |  x   |  x  |  -  |   x   |  x  |    -    | -  |  -  |  x  |    -    |      -     |   -   |


x=supported, /=not tested, o=only software emulation supported

Supported external Hardware
============================

The following external Hardware is supported:

  * TI TPS65381: Automotive 4.5V to 40V, 1.3A Buck Converter with 4 LDOs for Microcontroller over SPI
  * TI ADCS747x: 12-Bit ADC over SPI
  * Microchip MCP320X: 12-Bit ADC over SPI
  * MPU9250 / ICM-20948: Nine-Axis (Gyro + Accelerometer + Compass) MEMS (Compass not supported) over SPI
  * NTC Tempaturesensor over ADC

Software Emulation
==================

Some Hardware can be Emulated

  * Software Real time clock (Wall time, seconds and nanoseconds after 01/01/1970) using a HW Timer
  * Software Counter (counts GPIO Interrupts) use GPIO Interface 
  * Software PWM use a HW timer and GPIO

Software Support
================

  * TCP/UDP/IP Support over [lwIP][lwIP] over the generic Net Interface


[lwIP]: https://savannah.nongnu.org/projects/lwip/

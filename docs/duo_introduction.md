# RedBear Duo Introduction
---

![image](images/RBDuo.png)

* [Descriptions](#descriptions)
* [Features](#features)
* [Block Diagram](#block-diagram)
* [Pinouts](#pinouts)
* [Power Supply](#power-supply)
* [Development](#development)
* [Package Characteristics](#package-characteristics)
* [Layout Recommendations](#layout-recommendations)
* [Ordering Informations](#ordering-informations)
* [Resources](#resources)


## <span id="descriptions">Descriptions</span>

The [RedBear Duo](http://www.redbear.cc/duo) is a thumb-size development board designed to simplify the process of building Internet of Things (IoT) products. It is built with a powerful Cortext-M3 MCU, a wireless module which equips both Wi-Fi and BLE (Bluetooth Low Energy) connectivity, as well as abundant of peripherals. 

It enables you develop applications to communicate with other wireless accessories or your smart devices, e.g. mobile phone, tablet or computer, through BLE, Wi-Fi or both BLE and WiFi at the same time. If the Duo is connecting to a router which implemented internet capability, you can even communicate with the Duo through cloud. For example, you can just sit in your office and monitor the environment data sampled by the Duo at home.

The Duo supports several kinds of programming language, particularly like Arduino, C/C++, JavaScript and Python. You can develop the applications for Duo using GCC, Arduino IDE, Particle Web IDE, Espruino Web IDE and Broadcom WICED SDK.

The Duo is so powerful that you can be applied it to many applications, e.g.:

* Industrial Automation
* Building Automation
* Smart Home Appliances
* Smart Toys
* IoT Enabled Sensors
* WiFi / BLE Gateway
* Beacon Management


## <span id="features">Features</span>

* STMicroelectronics STM32F205, ARM 32-bit Cortex-M3 @120 MHz
* AMPAK AP6212A Wireless Module (built around Broadcom BCM43438):
    - Wi-Fi 802.11b/g/n, working on 2.4 GHz ISM Band
    - Bluetooth 4.1 (Dual Mode), working on 2.4 GHz ISM Band
* Memories:
    - 1MB internal flash
    - 2MB external SPI flash
    - 128KB SRAM
* User Interface:
    - 1 x RGB LED
    - 1 x single LED
    - 1 x RESET button 
    - 1 x user button
* 18 x Digital I/O
* 8 x Analog Input
* 13 x PWM
* Connectivity
    - 2 x UART
    - 2 x SPI
    - 1 x I2S
    - 1 x I2C 
    - 1 x High Speed USB
    - JTAG(SWD) debug port
* Development Platform: 
    - Arduino IDE
    - Particle Build(WebIDE)
    - Espruino WebIDE
    - Broadcom WICED SDK
    - ARM GCC
* Real-time operating system (FreeRTOS)
* Hardware and software open source
* Single-sided PCBA for easy mounting on other PCB
* Alternative signal chip antenna or external antenna
* FCC and CE certified


## <span id="block-diagram">Block Diagram</span>

![image](images/Duo_BlockDiagram.png)


## <span id="pinouts">Pinouts</span>

![image](images/RBDuo_Pinout.png)


## <span id="power-supply">Power Supply</span>

**!!! Caution: Use only one power source at a time, otherwise you will damage the board!**

To make the Duo board work normally, the board level working voltage (VCC) should range from **3.0v ~ 3.6v**. If the working voltage less than 3.0v, the wireless module would not work well, and if more than 3.6v, the target MCU would be damaged.

#### Power from Micro USB port

Connect the Duo to a 3.5v ~ 8v power source or to a computer via micro USB cable, will power up the Duo. The input voltage from the USB port will be regulated to 3.3v by the on-board regulator first and then supply the whole board circuit units. In this case, the `VIN` pin will output a voltage nearly to the USB port input voltage and the `3V3` pin will output a voltage equal to the board level voltage, i.e. 3.3v. Then the `VIN` pin can be invoked to power other high voltage drivered devices, e.g. Relays, Servers, Motors and etc. As well as the `3V3` pin can be invoked to power other 3.3v devices.

#### Power from VIN pin

Connect the `VIN` pin to a 3.5v ~ 8v power source will power up the Duo. The input voltage from the `VIN` pin will be regulated to 3.3v by the on-board regulator first and then supply the whole board circuit units. In this case, the `3V3` pin will output a voltage equal to the board level voltage, i.e. 3.3v. Then the `3V3` pin can be invoked to power other 3.3v devices.

#### Power from 3V3 pin

Connect the `3V3` pin to a 3.0 ~ 3.6 power source will also power up the Duo. The voltage from this pin directly suppies the whole board circuit units.

#### Power from VBAT pin

The voltage from `VBAT` should range from 1.8v to 3.6v, but it can NOT power up the Duo. According to the STM32F205 technical reference manual, VBAT pin can be connected to an optional standby voltage supplied by a battery or by another source to retain the content of the RTC backup registers, backup SRAM, and supply the RTC when VDD is turned off.


## <span id="development">Development</span>

* [Out-of-Box Experience](out_of_box_experience.md)
* [Getting Started with Arduino IDE](getting_started_with_arduino_ide.md)
* [Getting Started with Particle Build]()
* [Applications Development Guide](applications_development_guide.md)
* [Firmware Architecture Overview](firmware_architecture_overview.md)
* [RedBear discussion forum](http://discuss.redbear.cc/)


## <span id="package-characteristics">Package Characteristics</span>

![image](images/Duo_Package.png)


## <span id="layout-recommendations">Layout Recommendations</span>

![image](images/Duo_Layout_Recommend.png)
* Dimensions are in millimeters.


## <span id="ordering-informations">Ordering Informations</span>

* [RedBear Store](https://store.redbear.cc/product.html)
* [Worldwide Resellers](http://redbearlab.com/buy/)


## <span id="resources">Resources</span>

* [Modified Particle firmware source code](https://github.com/redbear/firmware)
* [Arduino board package for Duo](https://github.com/redbear/STM32-Arduino)
* [Modified Espruino source code](https://github.com/redbear/Espruino)
* [Modified MicroPython source code](https://github.com/redbear/micropython)
* [WICED SDK patch for Duo](https://github.com/redbear/WICED-SDK)
* [BTStack source code](https://github.com/redbear/btstack)
* [RedBear Duo schematic](https://github.com/redbear/Duo/tree/master/hardware/schematic)
* [Components datasheet](https://github.com/redbear/Duo/tree/master/hardware/datasheets)
* [FCC & CE certification](https://github.com/redbear/Duo/tree/master/certs)


## License

Copyright (c) 2016 Red Bear

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

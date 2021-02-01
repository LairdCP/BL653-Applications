BL653 smartBASIC-Applications
=============================

A repository for smartBASIC applications that run on the Laird Connectivity BL653 and BL653u (Released under the ISC License).

BL653 Overview
------------
Laird Connectivity’s BL653 contains the latest generation silicon with Bluetooth Low Energy v5.2 capabilities and groundbreaking ultra-low power performance. Building on the expertise of the BL600, BL652 and BL654 Series, the BL653’s class-leading Nordic nRF52833 silicon, optimized low power schemes and smartBASIC programming language provide a secure, stable, hostless Bluetooth environment. The BL653 introduces Bluetooth v5, bringing long range connectivity, industrial security and feature expansion to Laird Connectivity’s proven Bluetooth Low Energy modules. Let Laird Connectivity’s innovative BL653 series and decades of expertise in Bluetooth module design speed your product to market.

UwTerminalX
-----------
UwTerminalX is a cross-platform utility for communicating and downloading applications onto the BL653. The latest releases are available at https://github.com/LairdCP/UwTerminalX/releases

BL653 Documentation
-------------------
Documentation for the BL653 and BL653u can be found on the [Laird Connectivity BL653 website](https://www.lairdconnect.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/bl653-series-bluetooth-51-802154-nfc-module) and [BL653u website](https://www.lairdconnect.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/bl653-micro-series-bluetooth-51-802154-nfc-modules) including a [quick start guide for using the AT interface application](https://www.lairdconnect.com/documentation/quick-start-guide-bl65x-interface)

Older firmwares
-------------------------------
The files in this repository are designed for use with the latest BL653 firmware, which at the time of writing is 30.2.3.0. For applications targeting older firmware, please check the [Releases tab](https://github.com/LairdCP/BL653-Applications/releases)

Best Practices for Writing smartBASIC Applications
-------------------------------
1. Always check the resultcode returned from an API function. Non-zero result codes usually indicate that the operation has not been successful.
2. smartBASIC is event driven; ensure that the application is written in an event-driven manner. Starting with a state-machine or a flowchart is highly recommended.
3. Minimize the use of WAITEVENTs; ideally, WAITEVENT should be used only once at the end of the program to ensure the app is simple and robust.
4. Minimize radio usage when possible to save power.
5. Use comments wherever possible to ensure that the application can be read and understood.
6. Only hard-code when necessary. When hard-coding, use #defines to give meaning to the constants used.
7. Follow the smartBASIC app template found [here](https://github.com/LairdCP/BL653-Applications/blob/master/Applications/ttt.template.sb).

Notes
-------------------------------
Please note that for simplicity reasons, some sample apps have been written without important features such as error handling or result code checking. However, when writing your applications, please ensure that result codes returned from the API functions are always checked to ensure that your applications are robust and bug-free.

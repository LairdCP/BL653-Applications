--------
Feb 2022
--------

This folder contains smartBASIC applications that when loaded in a BL653
module will expose an AT interface or act as a BT510/BT610 repeater or act as a
BT510/BT610 gateway.

The repeater functionality resends all BT510/BT610 adverts as new adverts.
S130=5

The gateway functionality sends all BT510/BT610 advert data out via the uart
(@ 115200,N,8,1)
S130=3

The AT mode will allow AT commands to be sent over the uart interface
(@ 115200,N,8,1) to make it do various BLE, NFC or GPIO actions.
S130=0

     ==============================================================
     The minimum firmware version that you will need is as follows:

                             BL653 : v30.2.3.0

      The command 'AT I 3<cr>' will return the version number from
      the module
     ==============================================================

The folder contains many smartBASIC source code files which end with the
extension ".sb"

For BL653, use with file "$autorun$.BTx10.repeater.BL653.sb"

Note that there is insufficient flash space on the BL653 module for
$autorun$.BTx10.gateway.parsed.debug.sb and $autorun$.BTx10.repeater.debug.sb
If these files are needed, they can be loaded on to a BL654.

An application is downloaded to a module using a free Laird utility called
UwTerminalX. You can download the utility from ...

    https://github.com/LairdCP/UwTerminalX/releases

Only files that start with "$autorun$" are stand alone.
  DO NOT SELECT ANY FILES TO DOWNLOAD THAT DOES NOT START WITH "$autorun$

All other files are library files which are #included in the stand alone
files and if you try to download them to a module you will get one or
more download errors. To make that clear, all library files start with
a filename "$LIB$."

When an app is downloaded it will be saved in the module's file system as
a file called "$autorun$" which means it will automatically run when the
module is reset or powered up.

QUICK START GUIDE
Once an application is downloaded using UwTerminalX, power cycle the module.
Then send the command ATI0<cr> where <cr> is the enter key and you will
see the module respond with the name of the module and then an "OK" response.

DOCUMENTATION
There are two main documents that are relevant for this application which
can be found at

  https://www.lairdconnect.com/wireless-modules/bluetooth-modules/bluetooth-5-modules/BL653-series-bluetooth-module-nfc

   (1) BT510 Repeater/Gateway Application User Guide

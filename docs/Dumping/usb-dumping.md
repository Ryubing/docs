---
title: USB Dumping
---
Basic setup, can be skipped if you already followed this guide: [Switch modding](https://switch.hacks.guide/)
=======
- Download the latest archive of the [Rewrite NROs](https://github.com/DarkMatterCore/nxdumptool/releases), and copy them to your SD card, somewhere in the switch/ directory.
- Open the NRO on your console
- Plug the console in via USB
- Download [Zadig](https://zadig.akeo.ie/) and open it. It will require Administrator rights to run, as it needs to install a driver.
- Open Zadig, and select the device named nxdt_rw_poc.
- Change the WinUSB entry on the "Driver" line to libusbK, and then hit the button below that labeled "Install Driver"
- Unplug the USB cable and then plug it back in.

USB-dumping
=======
- Use the [Host EXE](https://github.com/DarkMatterCore/nxdumptool/releases) found inside 
`nxdt_host.7z` download.

![image](uploads/189e48c53030a1e323f572d9982af8aa/image.png)
- Click the big "Start Server" button

![image](uploads/9768548301a7927f63e234c42e996c74/image.png){width=25%}
- On your console, change the "Output Storage" setting to usb host (pc)

![image](uploads/47c2876899bcb62c64f73062b055eac6/image.png)
- Start dump on your console, and watch it transfer directly to your machine!
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

![image](https://github.com/Ryubing/Assets/blob/main/docs/guides/dumping/ndxt_host_image.png?raw=true)

- Click the big "Start Server" button
![image](https://github.com/Ryubing/Assets/blob/main/docs/guides/dumping/nxdt_host_ui_image.png?raw=true)

- On your console, change the "Output Storage" setting to usb host (pc)
![image](https://github.com/Ryubing/Assets/blob/main/docs/guides/dumping/nxdt_changeoutputstorage.png?raw=true)

- Start dump on your console, and watch it transfer directly to your machine!
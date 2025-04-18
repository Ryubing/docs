What You Need
=======
    Unpatched/Modchipped Switch
    Lockpick_RCM
    MicroSD Card (64GB+)

Backup Switch Keys
=======
- Download [Lockpick_RCM](https://git.ryujinx.app/-/project/7/uploads/77f6439f727b8249c8acfca650ac98a5/Lockpick_RCM.bin) unless you already have it.
- Put the `Lockpick_RCM.bin` into the `bootloader/payloads` folder on your microSD card.
- Boot `Hekate` and launch Lockpick_RCM.bin from the payloads tab.
  ![hekate](https://github.com/Ryubing/Assets/raw/refs/heads/main/docs/guides/dumping/hekate.bmp)

- Select `Dump from sysNAND`. Lockpick_RCM will dump the `prod.keys`, `title.keys` and `dev.keys` to the `switch folder` on your microSD card.
- Exit back to the Lockpick_RCM home screen.
- If you have games installed to emuNAND you can dump title.keys by selecting Dump from EmuNAND in Lockpick_RCM.
- Either: 
    - reboot to `Hekate` choose `tools` --> `USB Tools` --> `SD card` under USB Mass Storage while connected to your PC;
    - or power off and copy the prod.keys, title.keys and dev.keys from the `switch` folder on your microSD card to your PC.

  ![](https://github.com/Ryubing/Assets/raw/refs/heads/main/docs/guides/dumping/hekate_tools-tab.bmp) ![nyx20250410_050310](https://github.com/Ryubing/Assets/raw/refs/heads/main/docs/guides/dumping/hekate_usbtools.bmp)
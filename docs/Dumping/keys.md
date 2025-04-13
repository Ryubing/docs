---
title: Keys
---

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

  ![hekate](uploads/b75c7d5b3b748f46874870827410968a/hekate.bmp){width=25%}
- Select `Dump from sysNAND`. Lockpick_RCM will dump the `prod.keys`, `title.keys` and `dev.keys` to the `switch folder` on your microSD card.
- Exit back to the Lockpick_RCM home screen.
- If you have games installed to emuNAND you can dump title.keys by selecting Dump from EmuNAND in Lockpick_RCM.
- Either reboot to `Hekate` choose `tools` --> `USB Tools` --> `SD card` under USB Mass Storage while connected to your PC or power off and copy the prod.keys, title.keys and dev.keys from the `switch folder` on your microSD card to your PC.

  ![nyx20250410_050300](uploads/73f80410000c12f0c4a762a5f9dce98d/nyx20250410_050300.bmp){width=25%} ![nyx20250410_050310](uploads/b02774763a3ab5b84d9389b8dd7066fe/nyx20250410_050310.bmp){width=25%}
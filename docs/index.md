<table align="center">
    <tr>
        <td align="center" width="25%">
            <img src="https://raw.githubusercontent.com/Ryubing/Assets/refs/heads/main/RyujinxApp_1024.png" alt="Ryujinx" >
        </td>
        <td align="center" width="75%">
          
<h1>Ryujinx<h1>

<a href="https://github.com/Ryubing/Stable-Releases/releases/latest">
  <img src="https://img.shields.io/github/v/release/Ryubing/Stable-Releases?label=stable" alt="Stable Releases">
</a>

<a href="https://github.com/Ryubing/Canary-Releases/releases/latest">
  <img src="https://img.shields.io/github/v/release/Ryubing/Canary-Releases?label=canary" alt="Canary Releases">
</a>
<br>
<a href="https://discord.gg/PEuzjrFXUA">
<img src="https://img.shields.io/discord/1294443224030511104?color=5865F2&label=Ryubing&logo=discord&logoColor=white" alt="Discord">
</a>
        </td>
    </tr>
</table>

<p align="center">
  Ryujinx is an open-source Nintendo Switch emulator, originally created by gdkchan, written in C#.
  This emulator aims at providing excellent accuracy and performance, a user-friendly interface and consistent builds.
  It was written from scratch and development on the project began in September 2017.
  Ryujinx is available on a self-managed GitLab instance under the <a href="https://git.ryujinx.app/ryubing/ryujinx/-/blob/master/LICENSE.txt?ref_type=heads" target="_blank">MIT license</a>.
  <br />
</p>
<p align="center">
  On October 1st 2024, Ryujinx was discontinued as the creator was forced to abandon the project.
  <br>
  This fork is intended to be a QoL uplift for existing Ryujinx users.
  <br>
  This is not a Ryujinx revival project. This is not a phoenix project.
</p>

<p align="center">
    <img src="https://github.com/Ryubing/Assets/blob/main/docs/various-ryujinx-windows.png?raw=true" alt="Ryujinx example">
</p>

## Usage

To run this emulator, your PC must be equipped with at least 8GiB of RAM;
failing to meet this requirement may result in a poor gameplay experience or unexpected crashes.

## Latest build

Stable builds are made every so often, based on the `master` branch, that then gets put into the releases you know and love.
These stable builds exist so that the end user can get a more **enjoyable and stable experience**.
They are released every month or so, to ensure consistent updates, while not being an annoying amount of individual updates to download over the course of that month.

You can find the latest stable release [here](https://github.com/Ryubing/Stable-Releases/releases/latest).

??? warning "Canary builds"
    Canary builds are compiled automatically for each commit on the `master` branch.
    While we strive to ensure optimal stability and performance prior to pushing an update, these builds **may be unstable or completely broken**.
    These canary builds are only recommended for experienced users.

    You can find the latest canary release [here](https://github.com/Ryubing/Canary-Releases/releases/latest).

## Features

??? info "Audio"
    Audio output is entirely supported, audio input (microphone) isn't supported.
    We use C# wrappers for [OpenAL](https://openal-soft.org/), and [SDL2](https://www.libsdl.org/) & [libsoundio](http://libsound.io/) as fallbacks.

??? info "CPU"
    The CPU emulator, ARMeilleure, emulates an ARMv8 CPU and currently has support for most 64-bit ARMv8 and some of the ARMv7 (and older) instructions, including partial 32-bit support.<br/>
    It translates the ARM code to a custom IR, performs a few optimizations, and turns that into x86 code.
    <br/>
    There are three memory manager options available depending on the user's preference, leveraging both software-based (slower) and host-mapped modes (much faster).
    <br/>
    The fastest option (host, unchecked) is set by default.
    <br/>
    ???+ tip "PPTC"
        Ryujinx also features an optional Profiled Persistent Translation Cache, which essentially caches translated functions so that they do not need to be translated every time the game loads.
        <br/>
        The net result is a significant reduction in load times (the amount of time between launching a game and arriving at the title screen) for nearly every game.
        NOTE: This feature is enabled by default in the Options menu > System tab.
        You must launch the game at least twice to the title screen or beyond before performance improvements are unlocked on the third launch!
        These improvements are permanent and do not require any extra launches going forward.

??? info "GPU"
    The GPU emulator emulates the Switch's Maxwell GPU using either the OpenGL (version 4.5 minimum), Vulkan, or Metal (via MoltenVK) APIs through a custom build of OpenTK or Silk.NET respectively.
    <br/>
    There are currently six graphics enhancements available to the end user in Ryujinx: Disk Shader Caching, Resolution Scaling, Anti-Aliasing, Scaling Filters (including FSR), Anisotropic Filtering and Aspect Ratio Adjustment.
    These enhancements can be adjusted or toggled as desired in the GUI.

??? info "Input"
    We currently have support for keyboard, mouse, touch input, Joy-Con input support, and nearly all controllers.
    Motion controls are natively supported in most cases; for dual-JoyCon motion support, DS4Windows or BetterJoy are currently required.
    In all scenarios, you can set up everything inside the input configuration menu.

??? info "DLC & Modifications"
    Ryujinx is able to manage add-on content/downloadable content through the GUI.
    Mods (romfs, exefs, and runtime mods such as cheats) are also supported;
    the GUI contains a shortcut to open the respective mods folder for a particular game.

??? info "Configuration"
    The emulator has settings for enabling or disabling some logging, remapping controllers, and more.
    You can configure all of them through the graphical interface or manually through the config file, `Config.json`, found in the Ryujinx data folder which can be accessed by clicking `Open Ryujinx Folder` under the File menu in the GUI.

## License

This software is licensed under the terms of the [MIT license](https://git.ryujinx.app/ryubing/ryujinx/-/blob/master/LICENSE.txt?ref_type=heads).
This project makes use of code authored by the libvpx project, licensed under BSD and the ffmpeg project, licensed under LGPLv3.
See [LICENSE.txt](https://git.ryujinx.app/ryubing/ryujinx/-/blob/master/LICENSE.txt?ref_type=heads) and [THIRDPARTY.md](https://git.ryujinx.app/ryubing/ryujinx/-/blob/master/distribution/legal/THIRDPARTY.md?ref_type=heads) for more details.

## Credits

- [LibHac](https://github.com/Thealexbarney/LibHac) is used for our file-system.
- [AmiiboAPI](https://www.amiiboapi.com) is used in our Amiibo emulation.
- [ldn_mitm](https://github.com/spacemeowx2/ldn_mitm) is used for one of our available multiplayer modes.
- [ShellLink](https://github.com/securifybv/ShellLink) is used for Windows shortcut generation.

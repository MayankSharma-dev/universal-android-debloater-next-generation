# Universal Android Debloater Next Generation

**DISCLAIMER**: Use at your own risk. We're not responsible for anything that
could happen to your phone.

<img src="/resources/screenshots/v0.6.2.png" width="850" alt="uad_screenshot">

**This software is still in an early stage of development. Check out the issues, and feel free to contribute!**

**For real-time communication, consider joining our Discord server:**
[![](https://dcbadge.vercel.app/api/server/YHujHzA57a)](https://discord.gg/YHujHzA57a)

## Summary

This is a detached fork of the [UAD project](https://github.com/0x192/universal-android-debloater), which aims to improve privacy and battery performance by removing unnecessary and obscure system apps.
This can also contribute to improving security by reducing [the attack surface](https://en.wikipedia.org/wiki/Attack_surface).

Packages are as well documented as possible to provide a better understanding of what you can delete or not. The worst issue that could happen is removing an essential system package needed during boot causing then an unfortunate bootloop. After about 5 failed system boots, the phone will automatically reboot in recovery mode, and you'll have to perform a FACTORY RESET. Make a backup first!

In any case, you **CANNOT** hard-brick your device with this software! That's the main point, right?

## Features

- [x] Uninstall/Disable and Restore/Enable system packages
- [x] Multi-user support (e.g. apps in work profiles)
- [x] Export/Import your selection in `uad_exported_selection.txt`
- [x] Multi-device support: you can connect multiple phones at the same time
- [x] All your actions are logged, so you never forget what you've done

NB: System apps cannot truly be uninstalled without root (see the [FAQ](https://github.com/Universal-Debloater-Alliance/universal-android-debloater/wiki/FAQ))

## Universal Debloat Lists

- [x] GFAM (Google/Facebook/Amazon/Microsoft)
- [x] AOSP
- [x] Manufacturers (OEM)
- [x] Mobile carriers
- [x] Qualcomm / Mediatek / Miscellaneous

## Manufacturers debloat lists
* [ ] Archos
* [X] Asus
* [ ] Blackberry
* [X] Fairphone
* [ ] Gionee
* [X] Google
* [x] Honor
* [ ] HTC
* [X] Huawei
* [X] iQOO
* [X] LG
* [X] Lenovo
* [X] Motorola
* [X] Nokia
* [X] Nubia
* [X] Nothing Phone
* [X] OnePlus
* [X] Oppo
* [X] Realme
* [X] Samsung
* [X] Sony
* [X] Tecno
* [X] TCL
* [X] Unihertz
* [X] Vivo/iQOO
* [X] Wiko
* [X] Xiaomi
* [X] ZTE

## Mobile carriers debloat lists

| Country | Carriers                        |
| ------- | ------------------------------- |
| France  | Orange, SFR, Free, Bouygues     |
| USA     | T-Mobile, Verizon, Sprint, AT&T |
| Germany | Telekom                         |
| UK      | EE                              |

## How to use it

- **Read the [FAQ](https://github.com/Universal-Debloater-Alliance/universal-android-debloater/wiki/FAQ)!**
- **Do a proper backup of your data! You can never be too careful!**
  - Stuck in a bootloop? Check out [this FAQ item](https://github.com/Universal-Debloater-Alliance/universal-android-debloater-next-generation/wiki/FAQ#help-my-phone-is-stuck-in-a-bootloop).
- Enable _Developer Options_ on your smartphone.
- Turn on _USB Debugging_ from the developer panel.
- From the settings, disconnect from any OEM accounts (when you delete an OEM
  account package it could lock you on the lock screen because the phone can't
  associate your identity anymore)
- Install ADB (see the instructions by clicking on your OS below):
  <p>
  <details>
  <summary>LINUX</summary>

  - Install _Android platform tools_ on your PC :

  Debian Base:

  ```bash
  sudo apt install android-sdk-platform-tools
  ```

  Arch-Linux Base:

  ```bash
  sudo pacman -S android-tools
  ```

  Red Hat Base:

  ```bash
  sudo yum install android-tools
  ```

  OpenSUSE Base:

  ```bash
  sudo zypper install android-tools
  ```

  Gentoo Base:

  ```bash
  sudo emerge -av dev-util/android-tools
  ```

  NixOS Base:

  ```bash
  sudo nix-shell -p android-tools
  ```
  
  Alpine Linux or FreeBSD Base:

  ```bash
  sudo pkg install android-tools
  ```
  
  Fedora Base:
  
  ```bash
  sudo dnf install android-tools
  ```
  
  Replace sudo with doas depending on what you use
  
  </details>
  </p>

  <p>
  <details>
  <summary>MAC OS</summary>

  - Install [Homebrew](https://brew.sh/)
  - Install _Android platform tools_

    ```bash
    brew install android-platform-tools
    ```

  </details>
  </p>

  <p>
  <details>
  <summary>WINDOWS</summary>

  - Download [android platform tools](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
    and unzip it somewhere.
  - [Add the android platform tools to your PATH](https://www.architectryan.com/2018/03/17/add-to-the-path-on-windows-10/)
    **OR** make sure to launch UAD-ng from the same directory.

  - [Install USB drivers for your device](https://developer.android.com/studio/run/oem-usb#Drivers)
  - Check your device is detected:

    ```bash
     adb devices
    ```

  </details>
  </p>

- Download the latest release of UAD-ng for your Operating System [here](https://github.com/Universal-Debloater-Alliance/universal-android-debloater/releases). Take the `opengl` version only if the default version (with a Vulkan backend) doesn't launch.

**NOTE:** Chinese phone users may need to use the AOSP list to remove some stock
apps because those Chinese manufacturers (especially Xiaomi and Huawei) have been
using the name of AOSP packages for their own (modified & closed-source) apps.

**IMPORTANT NOTE:** You will have to run this software whenever your OEM pushes
an update to your phone as some _uninstalled_ system apps could be reinstalled.

## How to contribute

Hey-hey-hey! Don't go away so fast! This is a community project.
That means we need you! We're sure you want to make this project better anyway.

==> [How to contribute](https://github.com/Universal-Debloater-Alliance/universal-android-debloater/wiki)

## Special thanks

- [@mawilms](https://github.com/mawilms) for his LotRO plugin manager ([Lembas](https://github.com/mawilms/lembas))
  which helped me a lot to understand how to use the [Iced](https://github.com/hecrj/iced)
  GUI library.
- [@casperstorm](https://github.com/casperstorm) for the UI/UX inspiration.

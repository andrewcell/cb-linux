<br>

# 🙼 ＢＲＥＡＴＨ 

<p align="center">An experimental way to natively run 🅻🅸🅽🆄🆇 on modern Chromebooks without replacing firmware</p>

## Supported Devices

All Chromebooks released after 2018 are supported.

However, this project is being developed on `Nami`, so the following models will have for-sure audio support:
* Acer Chromebook 13 / Spin 13
* Dell Inspiron 14 2-in-1 Model 7486 
* Yoga Chromebook C630
* HP Chromebook x360 14 (i3 8130u)
* Acer Chromebook 715
* Acer Chromebook 714
* HP Chromebook 15 G1
* Dell Inspiron Chromebook 14 (7460)

> Stock Ubuntu requires a change in firmware (UEFI or Legacy Boot) and has everything except touchscreen and audio working. This project requires no change in firmware and has all peripherals working on my HP Chromebook 14 x360.

## Running Breath

Due to licensing restraints, you cannot just download an ISO of Breath and flash it. Instead, you *build* the bootable USB.
> Currently, this project only works on Debian or Ubuntu. Arch and Fedora support is planned.

Prerequisite: Git is installed

1. `git clone https://github.com/MilkyDeveloper/cb-linux && cd cb-linux`
2. `bash setup.sh`

Done! Now just boot into ChromeOS and run:
```
sudo crossystem dev_boot_usb=1; sudo crossystem dev_boot_signed_only=0; sync
```
to enable USB and Custom Kernel Booting.

Reboot, and with the USB plugged in, press <kbd>CTRL</kbd> <kbd>U</kbd>. After a black screen for 10 seconds, the system should display a login screen.
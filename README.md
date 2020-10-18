# ChromeJaro
Manjaro, for chromebook.

# Whats ChromeJaro?
ChromeJaro, is a instruction of how to install Manjaro, on your chromebook.

# Requirements 
0. Chromebook
1. Developer Mode turned on
2. SD Card or USB Drive with 32 GB or more
3. Manjaro iso
4. USB Mouse (Not required but will make things easier)

# Developer Mode
Firstly you will need to put the chromebook into developer mode, (Warning this will wipe all your local data). To do this, with the chromebook turned off, hold down the `esc`+ `refresh` keys and hit the power button. Follow the on screen options and the chromebook will reboot, you will see a scary white screen after the reboot. At this screen press the `ctrl`+ `D` keys together and your chromebook will reboot into chromeos.

# Preparing the USB or SD Card
Logon to your chromebook and download the manjaro .iso https://manjaro.org/download (any flavour I used the KDE version). Open a cros terminal `ctrl` + `T` and type `shell`. Navigate to your downloads folder 'cd ~\Downloads' and conform the .iso is there 'ls'. Now plug your usb stick in and work out its name by using lsblk it should be \dev\sdb if there are no other devices plugged into the system. Write the .iso to the usb (Warning this will erase all data on the USB stick) using `sudo dd if=manjaro.iso of=/dev/sdX' where sdX is in my case sdb but may be different in yours. This can take up to 5 minuntes, once finished eject and remove the USB stick.

# Enabling Legacy and USB Boot
ChromeOS Firmware Utility Script
The ChromeOS Firmware Utility Script simplifies the most common functions most users need when interacting with the firmware on their ChromeOS device. It can be run from ChromeOS, or any Linux which has a full Bash shell (so LibreELEC users need to boot a Ubuntu Live USB (eg) and run it from there). Currently, it allows the user to:

Install/Update the RW_LEGACY firmware with a newer/working/customized version of the SeaBIOS firmware payload
Install/Update coreboot/UEFI (Full ROM) firmware, built from the latest sources
Set the Boot Options (GBB Flags) (only for stock ChromeOS firmware)
Set the device's Hardware ID (only for stock ChromeOS firmware)
Remove the ChromeOS Developer/Recovery mode Bitmaps (only for stock ChromeOS firmware)
Restore the ChromeOS Bitmaps (only for stock ChromeOS firmware)
Restore the Stock BOOT_STUB
Restore the Stock Firmware
At startup, the Firmware Utility Script will automatically detect the device, OS, and current firmware details, and show a customized menu options based on this information. Some options may be greyed-out/disabled for some devices. Because most of these operations are being done to normally read-only parts of the firmware, the firmware write protect will need to be removed for most of the script's functions. This is documented for each function below, and the script will likewise check and display the write-protect state for each function that requires it to be disabled.

IMPORTANT:
Due to recent changes in ChromeOS' security settings, a new set of commands must be used to run the Firmware Utility Script under ChromeOS. Running it under Linux can use the same old one-line command.
Also, you must execute these commands **as a normal/non-root user**. Running them as root will break things.

To download and run this script under ChromeOS, from a terminal/shell type:
cd; curl -LO mrchromebox.tech/firmware-util.sh
sudo install -Dt /usr/local/bin -m 755 firmware-util.sh
sudo firmware-util.sh
and press enter. (copy/paste these to avoid typos)

To download and run this script under Linux, from a terminal/shell type:
cd; curl -LO mrchromebox.tech/firmware-util.sh && sudo bash firmware-util.sh
and press enter.
NOTE: Under ChromeOS, this script must be run from a crosh shell (CTRL+ALT+T, 'shell', enter) or VT2 (CTRL+ALT+F2, login 'chronos'); it cannot be run from a crostini (penguin) terminal as that is a virtualized container and lacks the necessary access to read or modify the firmware.

There will be something like this.
https://imgur.com/a/6CLZR9N
 Click 1 and enter
 It might prompt you to do stuff.
 
 # Installing Manjaro
 Now everything is set and ready to go insert your freshly made manjaro USB stick and reboot the chromebook at on the white screen press `ctrl` + `L` to boot into the legacy bios. Once there it should auto boot from the USB stick, if not tap escape and select the USB stick from the list. The trackpad will not work at this point so it can be handy to have a USB mouse to help. Follow the onscreen install wizard paritioning how you like etc. Once the install is complete reboot and remove the USB stick, press `ctrl` + `L` to enter manjaro at the white boot screen. It will show a USB Drive, or a SD Card type the number that you want to boot to, then install manjaro under `-mmcblk0p1.
 
 # Sucessfully installed Manjaro!
 I hope this had worked, if it has not please, make a request.
 
 (CREDITS TO http://mjcliffe.blogspot.com/)
  
  


# T430-Hackintosh i5-3320M
Installing Sierra on a T430

All necessary Files for installing Sierra on this Machine.

All is working.

If you are using another CPU you can use the script from this repo:

https://github.com/Piker-Alpha/ssdtPRGen.sh

to generate a new SSDT which fits on your model.

If you are installing OS X/macOS for the first time on the machine and want to use internal Bluetooth you must patch the Firmware. To do that you must move the 3 Kexts:

BrcmFirmwareData / BrcmFirmwareRepo / BrcmPatchRAM2

into "Other" AND move BrcmBluetoothInjector.kext out of the "Other" Folder. Don´t use the 4 Kext at the same Time. If your first boot with the 3 Kexts is done you can remove them and move BrcmBluetoothInjector.kext back to "Other". Your BT Firmware was patched. Thats it.

To get the Sleepmode properly working you need to execute the following commands in the Terminal.

  sudo pmset hibernatemode 0
  sudo rm /var/vm/sleepimage
  sudo touch /var/vm/sleepimage
  sudo chflags uchg /var/vm/sleepimage

Done! Now enjoy your fully working Hackbook. (-:

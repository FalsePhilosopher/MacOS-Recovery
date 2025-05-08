# MacOS-Recovery
Recovery images for MacOS  
The images were downloaded from apple using [MacRecoveryX](https://github.com/AngeloAvv/MacRecoveryX) and converted using [dmg2img](https://github.com/Lekensteyn/dmg2img).

The release section has MacOS images compressed with zstd, download the img.zst, `unzstd` the .img.zst(winrar or 7zip on win, files on mac), `dd` the .img(Win32 Disk Imager on win or UNetbootin on win/mac) to a USB stick, power-on the Mac with the USB stick inserted while the Option/alt (⌥) key is pressed, select the USB stick, then reinstall MacOS.
```
wget https://github.com/FalsePhilosopher/MacOS-Recovery/releases/download/MacOS-15/MacOS-15-BaseSystem.img.zst
unzstd -T0 MacOS-15-BaseSystem.img.zst
dd if=MacOS-15-BaseSystem.img of=/dev/sdx #Replace sdx with the disk you want to write it to, run lsblk to find your disk name.
```
The images can also be used to create a MacOS VM, rename to BaseSystem.img and run [step 2](https://github.com/foxlet/macOS-Simple-KVM#step-2).

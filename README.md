# MacOS-Recovery
Recovery images for MacOS  
The images were downloaded from apple using [MacRecoveryX](https://github.com/AngeloAvv/MacRecoveryX) and converted using [dmg2img](https://github.com/Lekensteyn/dmg2img).

The release section has MacOS images compressed with zstd, download the image, unzstd the img, then dd the image to a drive and boot to usb by holding option.
```
wget https://github.com/FalsePhilosopher/MacOS-Recovery/releases/download/MacOS-15/MacOS-15-BaseSystem.img.zst
unzstd -T0 MacOS-15-BaseSystem.img.zst
dd if=MacOS-15-BaseSystem.img of=/dev/sdx #Replace sdx with the disk you want to write it to, run lsblk to find your disk name.
```
The images can also be used to create a MacOS VM, rename to BaseSystem.img and run [step 2](https://github.com/foxlet/macOS-Simple-KVM#step-2).

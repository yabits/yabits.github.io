# yabits: Fast and lightweight yet another UEFI implementation

[yabits](https://github.com/yabits/uefi) is a pure UEFI coreboot payload.
Compared with [TianoCore](https://www.tianocore.org/),
it is fast and lightweight.
yabits is based on the part of [Minoca OS](https://www.minocacorp.com/).
It can run GRUB2, Linux, OpenBSD, and other UEFI applications.
Tested on QEMU/KVM and Lenovo ThinkPad X230.
It is still under the development and not ready for production.

## Downloads

The latest yabits is [v0.0.1](https://github.com/yabits/uefi/releases/tag/v0.0.1).
This release is pre-release.
* `coreboot.com`: coreboot rom with yabits for `qemu-system-x86_64` machine type "pc-i440fx-2.8"
* `uefi`: yabits coreboot payload with debug infomation
* `uefi.elf`: stripped yabits coreboot payload

You can try yabits `coreboot.com` on QEMU.
Prepare UEFI-aware OS image.
Run

```
$ qemu-system-x86_64 -drive if=pflash,format=raw,readonly,file=coreboot.rom -drive file=os.qcow2,if=none,id=sata -device ich9-ahci,id=ahci -device ide-drive,drive=sata,bus=ahci.0 -serial stdio -m 2G
```

![GRUB2 booted from yabits](img/yabits-grub2.png "GRUB2 booted from yabits")

## Build from Source

## Demo

## Comparision

## License

yabits is lincesed under the terms of 
[GNU General Public Lincese, version 3](https://github.com/yabits/uefi/blob/master/LICENSE).
See the headers of source code for more details.

This page is 
[MIT](https://github.com/yabits/yabits.github.io/blob/master/LICENSE) 
license.

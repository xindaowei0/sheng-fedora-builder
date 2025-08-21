# Installation guide

<details>
  <summary><strong>Singleboot installation</strong></summary>

#### Reboot your tablet into bootloader mode by holding ```Volume Down``` and ```Power``` buttons

#### Flash boot image
```bash
fastboot flash boot_ab boot.img
```

#### Flash rootfs image
```bash
fastboot flash userdata root.img
```

#### Clear dtbo partition
```bash
fastboot erase dtbo
```

#### Exit bootloader mode
```bash
fastboot reboot
```

</details>

<details>
  <summary><strong>Dualboot installation</strong></summary>

### Dualboot notes
- Repartition required
- Recommended slots configuration: 
    - Slot A: Android
    - Slot B: Fedora linux
- To switch slot from linux use ```sudo qbootctl -s [a|b]```
- To switch slot from android use [Boot Control](https://github.com/capntrips/BootControl) app
- Disable Android OTA updates in settings. Otherwise it will override Fedora installation in the other slot

#### Reboot your tablet into bootloader mode by holding ```Volume Down``` and ```Power``` buttons

#### Flash boot image to slot b
```bash
fastboot flash boot_b boot.img
```

#### Flash rootfs image
```bash
fastboot flash fedora_partition_name_here root.img
```

#### Clear dtbo partition in slot b
```bash
fastboot erase dtbo_b
```

#### Exit bootloader mode
```bash
fastboot reboot
```
</details>

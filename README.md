# justinformentin additions
This repo works for any wifi adapter with the Realtek rtl8811au chipset. Just run this:

```sh
# sudo apt-get update
# sudo apt-get install linux-headers-generic build-essential git
# git clone https://github.com/abperiasamy/rtl8812AU_8821AU_linux.git
# cd rtl8812AU_8821AU_linux
# make
# sudo make install
# sudo modprobe rtl8812au
```

# rtl8812au

Realtek 8812AU/8821AU USB WiFi driver.

for AC1200 (801.11ac) Wireless Dual-Band USB Adapter

This code is base on version 4.3.14 from https://github.com/diederikdehaas/rtl8812AU

## Known Supported Devices:

```
* COMFAST 1200Mbps USB Wireless Adapter(Model: CF-912AC)
```

## Compiling with DKMS

```sh
# sudo make -f Makefile.dkms install
```

### Compiling for Raspberry Pi

Install kernel headers and other dependencies.

```sh
# sudo apt-get install linux-image-rpi-rpfv linux-headers-rpi-rpfv dkms build-essential bc
```

Append following at the end of your ``/boot/config.txt``, reboot your Pi

```sh
kernel=vmlinuz-3.10-3-rpi
initramfs initrd.img-3.10-3-rpi followkernel
```

Edit Makefile and turn on ``CONFIG_PLATFORM_ARM_RPI``, turn off ``CONFIG_PLATFORM_I386_PC``

```sh
CONFIG_PLATFORM_I386_PC = n
CONFIG_PLATFORM_ARM_RPI = y
```

```sh
# cd /usr/src/rtl8812au
# sudo make clean
# sudo make
# sudo make install
# sudo modprobe -a rtl8812au
```

## Contributors
<!-- DO NOT EDIT - CONTRIBUTORS.md is autogenerated from git commit log by contributors.sh script. -->

- Anand Babu (AB) Periasamy
- Andreas Hofmann
- Andrew Mann
- AndyPi
- Anton
- archshift
- bits3rpent
- Chen Minqiang
- Daiki Tamada
- Fjodor42
- gremsto
- HackDefendr
- Harshavardhana
- jjones-jr
- Joe
- Joe Acosta
- John Lenz
- Jos Dehaes
- Karl-Philipp Richter
- Marco Milanesi
- Mauro Ribeiro
- Maximilian Schwerin
- mpoly
- Nick Bartos
- Peter H. Li
- pgroenbech
- scrivy
- Taehan Stott
- Vicent Llongo
- Victor Azizi
- 赵迤晨 (Zhao, Yichen)

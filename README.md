# 8822BU for Linux

This is a fork of [https://github.com/EntropicEffect/rtl8822bu](https://github.com/EntropicEffect/rtl8822bu) and adds support for the TP-Link Archer T3U Plus. Building and installing using the instructions below has been tested in Arch Linux with kernel 5.10.15-arch1-1.

The following README is a modified version from the upstream repository.

---

Driver for 802.11ac USB adapters with the RTL8822BU chipset.
Only STA/Monitor modes are supported, no AP.  

A few known wireless cards that use this driver include: -
* [Edimax EW-7822ULC](http://us.edimax.com/edimax/merchandise/merchandise_detail/data/edimax/us/wireless_adapters_ac1200_dual-band/ew-7822ulc/)
* [ASUS AC-53 NANO](https://www.asus.com/Networking/USB-AC53-Nano/)
* [D-Link DWA-182 (Revision D1 only)](http://ca.dlink.com/products/connect/wireless-ac1200-dual-band-usb-adapter/)
* [TP-Link Archer T3U Plus](https://www.tp-link.com/us/home-networking/usb-adapter/archer-t3u-plus/)
* [TP-Link Archer T4U (Revision V3 only)](https://www.tp-link.com/us/home-networking/usb-adapter/archer-t4u/)

> NOTE: At least kernel v4.7 is needed to compile this module.

Currently tested on `X86_64` the platform **only**.

## Installing
To build, type  
```
make
```
in the source directory.

To install the module files, type
```
sudo make install
```


## DKMS
Install the module using DKMS: in the source directory type
```
sudo dkms add .
sudo dkms install -m 88x2bu -v 1.1
```

To uninstall the module, type
```
sudo dkms remove -m 88x2bu -v 1.1 --all
sudo rm -rf /usr/src/88x2bu-1.1
```

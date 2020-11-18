---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
title: Intel 10th gen Hackintosh build
---
Inspired by: https://github.com/roederja/asus-rog-strix-b460I-hackintosh

## Hardware buying list

* Case: [Fractal Design Era ITX Silver - White Oak](https://www.amazon.de/Fractal-Design-FD-CA-ERA-ITX-SI-Noir/dp/B07TQ8937V)
* MB: [ASUS ROG Strix B460-I Gaming](https://www.amazon.de/-/en/ROG-B460-I-Motherboard-Mini-ITX-Networking/dp/B088W9RZZF/ref=sr_1_3?dchild=1&keywords=ASUS+ROG+STRIX+B460-I&qid=1605740143&sr=8-3) good mb for non K cpus, and it have replaceable wifi card (hidden under back panel shield)
* CPU: [Intel Core I7 10700](https://www.amazon.de/-/en/Intel-Core-i7-10700-base-clock/dp/B0883NPRL9/ref=sr_1_4?dchild=1&keywords=intel+10700&qid=1605740310&sr=8-4) If u can - buy non box version, since in my build i go for water cooling
* CPU Cooler: [FRACTAL Design Celsius S24](https://www.amazon.de/-/en/Fractal-Design-Celsius-Black-240mm/dp/B0719DHG5Y/ref=sr_1_9?crid=397B295GK7CME&dchild=1&sr=1-9&th=1)
* RAM: [32GB (2x 16384MB) Corsair Vengeance LPX](https://www.amazon.de/-/en/Corsair-Vengeance-High-Performance-Desktop-Airflow/dp/B016ORTNI2/ref=sr_1_1?dchild=1&keywords=32+gb+%282x+16384mb%29+corsair+vengeance+lpx&qid=1605741069&sr=8-1)
* SSD: [Samsung 970 Evo Plus M.2](https://www.amazon.de/-/en/dp/B07MFBLN7K/ref=twister_B07N1DF97S?_encoding=UTF8&psc=1)
* Wifi+BT: [BCM94360NG](https://www.amazon.de/-/en/gp/product/B083YXS7VF/ref=ppx_yo_dt_b_asin_title_o04_s00?ie=UTF8&psc=1) Natively supported in macos
* PSU: [Corsair SF450](https://www.amazon.de/-/en/Corsair-SF450-450W-SFX-supply/dp/B01CK7KMB2/ref=sr_1_1?dchild=1&keywords=Corsair+SF+Series+SF450&qid=1605740962&sr=8-1) but basically any SFX (better not SFX-L) psu with cabel management
* Any 16gb+ usb flash stick

## Performance
* Cinebench R20: 4899

## Details

### BIOS
UPDATE BIOS TO LATEST VERSION!!!

Things I changed from default:
* Fast boot: OFF
* Intel Virtualization Technology: ON
* OS type: Windows UEFI
* Multi Monitor support: ON
* Clear the platform key as this disables secure boot.

### Prepare Usb
Follow [Dortania OpenCore-Install-Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/),
and to make it much easier: 
[U can get full EFI structure ready for this build from my repository](https://github.com/buldezir/buldezir.github.io/archive/main.zip),
after that from guide sections "Gathering files" and "config.plist Setup" 
u will need only GenSMBIOS part to generate your unique id (https://github.com/corpnewt/GenSMBIOS)

### Install
Install like normal Mac OS

### Use
Use like normal mac :) all features like handoff will work.
*The only bad side* with BCM94360NG my wifi work on speeds much lower than intended. basicaly some time after connection it drops to 27mbps.
After install follow [OpenCore-Post-Install](https://dortania.github.io/OpenCore-Post-Install/universal/oc2hdd.html#grabbing-opencore-off-the-usb) to make system bootable without usb

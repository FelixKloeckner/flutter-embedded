# Configuration file to build Flutter Embedded for Raspeberry Pi 3 with kas.

Translated from https://github.com/jwinarske/manifests

Install kas (version 3.1):
```
git clone https://github.com/siemens/kas.git -b 3.1
```

Download configuration and build image:
```
git clone https://github.com/FelixKloeckner/flutter-embedded.git
cd flutter-embedded
../kas/kas-container build kas-flutter-raspberrypi.yml
```

Write image (assuming sdcard as sdb):
```
cd build/tmp/deploy/images/raspberrypi3-64/
sudo bmaptool copy core-image-minimal-raspberrypi3-64.wic.bz2 --bmap core-image-minimal-raspberrypi3-64.wic.bmap /dev/sdb

```

Run flutter gallery on target:
attach monitor, keyboard, mouse
login as root
```
flutter-pi --release /usr/share/flutter/gallery
```

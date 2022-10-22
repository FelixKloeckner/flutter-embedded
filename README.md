# Configuration file to build Flutter Embedded for Raspeberry Pi with kas.

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

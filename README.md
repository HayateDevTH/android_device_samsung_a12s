## How To Compile

# Create dirs
```
mkdir twrp; cd twrp
```

## Init repo
```
repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
```

## Clone repo
```
git clone https://gitlab.com/HayateDevTH/android_device_samsung_a12s -b android-12.1 device/samsung/a12s
```
## Sync repo
```
repo sync -j$(nproc --all)
```
## Build
```
source build/envsetup.sh; export ALLOW_MISSING_DEPENDENCIES=true; lunch twrp_a12s-eng; mka recoveryimage
```

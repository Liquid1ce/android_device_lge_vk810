# android_device_lge_vk810 Coming soon

Follow instructions here
https://github.com/lj50036/platform_manifest_twrp_cm

created localmanifest.xml in local_manifests
cd .repo/local_manifests
vim localmanifest.xml

#<?xml version="1.0" encoding="UTF-8"?>
#<manifest>
#<remote name="vk810" fetch="https://github.com/Liquid1ce" />
#<project path="device/lge/vk810" name="android_device_lge_vk810" remote="vk810" revision="omni_twrp_mm"/>
#</manifest>


repo sync

source build/envsetup.sh
lunch omni_vk810-eng
make clean && make -j5 recoveryimage


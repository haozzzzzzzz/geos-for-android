# geos for android
haozi.
2015/04/29

Flow these steps below to build your geos's static library for android:

1. Download GEOS and extract it to this directory.
2. Open Terminal and run "./configure --build=x86_64-pc-linux-gnu --host=arm-linux-eabi"
3. Modify ./jni/Android.mk, and set GEOS_PATH.
4. Open Terminal and run "ndk-build".

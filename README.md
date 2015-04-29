# geos for android
haozi.
2015/04/29

Flow these steps below to build your geos's static library for android:

1. Download GEOS and extract it to this directory.
2. Open Terminal and run "./configure --build=x86_64-pc-linux-gnu --host=arm-linux-eabi"
3. Modify ./jni/Android.mk, and set the value of $(GEOS_PATH).
4. Open Terminal and run "ndk-build".

---------------------------------------------
MORE INFORMATION YOU NEED TO KNOW
---------------------------------------------
These original .mk file were seperated from spatialite-android ( https://github.com/aamenos/spatialite-android ),and they are related to geos-3.6.6. In order to build geos with higher version, You can modify the ./jni/Android.mk and add source file reference like "$(GEOS_PATH)/*.cpp".


------------------------------------------------------------------------------------
按以下步骤构建用于Android NDK的GEOS静态库:
1. 下载GEOS，将其解压到当前目录。
2. 打开Terminal，运行"./configure --build=x86_64-pc-linux-gnu --host=arm-linux-eabi"
3. 在./jni/Android.mk中添加$(GEOS_PATH)
4. 最后在Terminal中运行"ndk-build"即可。

---------------------------------------------
更多信息
---------------------------------------------
这些.mk文件是分离自spatialite-android ( https://github.com/aamenos/spatialite-android )，它们用于构建geos-3.6.6。你可以通过在./jni/Android.mk中手动添加源码去构建更高版本的GEOS,形如"$(GEOS_PATH)/*.cpp"。

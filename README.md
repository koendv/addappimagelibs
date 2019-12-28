# addappimagelibs
Automatically adds libraries to a Raspberry AppImage project.

## Description

```addappimagelibs``` determines which shared libraries an AppImage needs, and copies the libraries to the AppImage. Only libraries that are not installed on a *2019-09-26-raspbian-buster-full* are copied.

```addappimagelibs-qt``` adds Qt plugins and their dependencies as well.

## Example

A program using boost and wxwindows.

```
koen@raspberrypi:~/src/addappimagelibs $ find ./PrusaSlicer.AppDir/
./PrusaSlicer.AppDir/
./PrusaSlicer.AppDir/usr
./PrusaSlicer.AppDir/usr/bin
./PrusaSlicer.AppDir/usr/bin/prusa-slicer
koen@raspberrypi:~/src/addappimagelibs $ ./addappimagelibs ./PrusaSlicer.AppDir/
koen@raspberrypi:~/src/addappimagelibs $ find ./PrusaSlicer.AppDir/
./PrusaSlicer.AppDir/
./PrusaSlicer.AppDir/usr
./PrusaSlicer.AppDir/usr/lib
./PrusaSlicer.AppDir/usr/lib/libGLEW.so.2.1.0
./PrusaSlicer.AppDir/usr/lib/libboost_regex.so.1.67.0
./PrusaSlicer.AppDir/usr/lib/libwx_gtk2u_adv-3.0.so.0.4.0
./PrusaSlicer.AppDir/usr/lib/libboost_log_setup.so.1.67.0
./PrusaSlicer.AppDir/usr/lib/libwx_gtk2u_html-3.0.so.0.4.0
./PrusaSlicer.AppDir/usr/lib/libtbb.so.2
./PrusaSlicer.AppDir/usr/lib/libnlopt.so.0.8.2
./PrusaSlicer.AppDir/usr/lib/libwx_gtk2u_core-3.0.so.0.4.0
./PrusaSlicer.AppDir/usr/lib/libwx_gtk2u_gl-3.0.so.0.4.0
./PrusaSlicer.AppDir/usr/lib/libwx_baseu-3.0.so.0.4.0
./PrusaSlicer.AppDir/usr/lib/libboost_log.so.1.67.0
./PrusaSlicer.AppDir/usr/bin
./PrusaSlicer.AppDir/usr/bin/prusa-slicer
```





[![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/nt4f04uNd/sweyer) 

# Sweyer

This is an open-source non-commercial repo of music player that is built with flutter.
This app is just my sight on how UI/UX in music apps should be.
Currently I am building it only for Android

Some conventions that I use when I write my application can be found in [README_CONVENTIONS.md](https://github.com/nt4f04uNd/sweyer/blob/master/README_CONVENTIONS.md) file

## Demos

<img alt="" src="demos/1.gif" width="33%"><img alt="" src="demos/2.gif" width="33%" /><img alt="" src="demos/3.gif" width="33%" />

## In plans

* Albums and artists grouping support
* More extended playlist capabilities
* Full media buttons and maximum devices support
* Desktop widgets
* Desktop context menu
* Open music files with player
* Flexible personalization settings
* Exif-data editor
* Integration with some music API (lyrics, album arts, etc., maybe even machine learning)
* Color the interface based on the album art

## How to run Flutter in GitPod

After GitPod workspace creation the `flutter pub get` and `flutter doctor` should run, wait before they complete and ensure that all has installed correctly. 

Then:

1. [ON YOUR PC] Connect the device to your PC with `adb` via local network 
  
   Connect the device with USB and run the following two commands
   ```shell
   adb tcpip <PORT>
   adb connect <DEVICE_IP>:<PORT>
   ```
 
2. [ON YOUR PC] Install `ngrok` and run 
   
   ```ngrok tcp <DEVICE_IP>:<PORT>```

3. [IN GITPOD] Copy ngrok ip and port, they go after `tcp://`, and then run
   ```shell
   adb connect <NGROK_IP>
   flutter run
   ```
P.S. If you will then want to build it on your local machine, you should run `adb uninstall "com.nt4f04und.sweyer"` to uninstall the debug app completely, because the build licenses won't match and the following builds will fail.

<!-- ## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference. -->

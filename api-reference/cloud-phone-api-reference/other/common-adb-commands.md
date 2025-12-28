# Common ADB Commands

> API Reference > Cloud Phone API Reference > Other > Common ADB Commands

**Source:** [https://doc.geelark.com/web/#/602813392/101528668](https://doc.geelark.com/web/#/602813392/101528668)

---

## Common Commands
GeeLark Cloud Phone supports all Android **adb** commands. Below are some frequently used commands.To enable adb, please refer to: [https://help.geelark.com/adb](https://help.geelark.com/adb)

### Upload a file from your local computer to the cloud phone

```
adb push /Users/geelark/Downloads/movie.mp4 /sdcard/movie.mp4

```

### Download a file from the cloud phone to your local computer

```
adb pull /sdcard/movie.mp4 /Users/geelark/Downloads/movie.mp4

```

### Get cloud phone device ID

```
//Android 13：Version
adb shell getprop ro.boot.serialno
//other Android version：
adb shell getprop ro.serialno

```

### Get cloud phone environment ID

```
adb shell getprop ro.gl.serialno

```

### Capture the cloud phone screen and save it locally

```
adb exec-out screencap -p > /Users/geelark/Downloads/screenshot.png

```

### Record the cloud phone screen and save it locally

```
adb shell screenrecord /sdcard/demo.mp4
adb pull /sdcard/demo.mp4 /Users/geelark/Downloads/demo.mp4

```

### Install an app to the cloud phone

```
//（-r:recover，-g:grant permission）
adb install -r -g /Users/geelark/Downloads/tiktok.apk

```

### Uninstall an app

```
adb uninstall com.ss.android.ugc.aweme

```

### Tap on coordinates

```
// click(400,360)
adb shell input tap 400 360
// long lick(400,360)
adb shellinput swipe 400 360 400 360 1000
// swipe from(400,1200)to(400,100)
adb shellinput swipe 400 1200 400 100 1000

```
Setting up BOOX Note Air 2 Plus to be more privacy oriented

Michael Bazzell's ADB as mentioned in Extreme Privacy [Mobile devices chapter]

Process:

We will first need to power on the tablet and find advanced settings. 

We need to do this in order to be able to enable advanced debug mode, which will let us view all system processes via ADB in PowerShell.

After looking around, I cannot find it! What can I do?

We can install an app that gives us that option, via F-Droid. 

We can install F-Droid by accessing the online browser and downloading the APK.

After, we can load up F-Droid, find and install the Smart Quick Settings App.

Load up the app previously mentioned, then go to page 2 or 3 and find build number. Press that multiple times until we can enable developer mode.

Enable USB ADB setting.

Then get powershell on a desktop and enable adb

Then connect device via USB cable and test connection via ```adb devices``` command

```
adb shell pm list packages
adb shell pm list package | findstr 'google'
adb shell pm uninstall -k -user 0 process
```

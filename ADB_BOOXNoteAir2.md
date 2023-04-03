Setting up BOOX Note Air 2 Plus to be more privacy oriented

This guide was inspired by Michael Bazzell's mention of ADB in Extreme Privacy [Mobile devices chapter].

The purpose of this is to view the packages via Google's advanced debug settings in order to disable any packages that we would not like. Note that this can break functionality of features on your device, proceed with caution.

## Process:
**Note that the process will be done specifically for the BOOX Note Air 2 Plus, but any Android device with an internet connection should be able to follow.**

For this, we will need a laptop or desktop with Powershell, Bash, or a Terminal. Set-up guide to be inserted [INSERT HERE]

### Tablet side:

We will first need to power on the tablet and find advanced settings. 

We need to do this in order to be able to enable advanced debug mode, which will let us view all system processes via ADB in PowerShell.

After looking around, I cannot find it! What can I do?

We can install an app that gives us that option, via F-Droid. 

We can install F-Droid by accessing the online browser and downloading the APK, link here: https://f-droid.org/.

After, we can load up F-Droid, find and install the Smart Quick Settings App.

Load up the app previously mentioned, then go to page 2 or 3 and find build number. Press that multiple times until we can enable developer mode.

Enable USB ADB setting.

### Desktop side:

Then get powershell on a desktop and instal adb [ADB INSTALL GUIDE NEEDED HERE]

Then connect device via USB cable and test connection via ```adb devices``` command

You should notice at least one device connected now, if this is not the case, reboot your device - it needs to be on while connected!

```
adb shell pm list packages
adb shell pm list package | findstr 'google'
adb shell pm uninstall -k -user 0 process
```

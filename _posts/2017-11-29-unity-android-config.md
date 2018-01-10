---
excerpt: "How to set up Unity for Android development? How to download and install JDK, set Android SDK PATH and other Android stuff on Windows? Here you have step by step receipt to download & start Android development environment for Unity."
header:
  overlay_image: /assets/images/2017/android/cover.png
  overlay_color: "#333"
  overlay_filter: 0.5

title: "Configure Android development environment for Unity"
date: "2017-11-29 19:00:00"
categories: unity
---

This is quick guide to all things you need to do before start Unity Android development. I gathered there things that I was always looking for and didn't found on Unity documentation. From step where those instructions would double you'll be pointed to proper documentation page.

### 1. Download and install JDK

If you want to develop for Android you will need to install Java and set environment variables.

Open the [Oracle website](http://www.oracle.com/technetwork/java/javase/downloads/index.html) and download newest JDK.

![Oracle instructions A](/assets/images/2017/android/jdkA.png)

On the next view choose your version (Windows?):
![Oracle instructions B](/assets/images/2017/android/jdkB.png)

Then click through Java installer.

### 2. Setup Java environment variables
For Android / Unity purposes its only required to set up `PATH` variable. To do this you can install useful program called [Patheditor](https://patheditor2.codeplex.com/). Otherwise, you can google how to setup `PATH` environment variable.

![Patheditor](/assets/images/2017/android/patheditor.png)

If you would like to setup other environment variables for Java here are [the examples](https://stackoverflow.com/questions/1672281/environment-variables-for-java-installation):

```
JAVA_HOME : C:\Program Files\Java\jdk1.8.0_112
JDK_HOME : %JAVA_HOME%
JRE_HOME : %JAVA_HOME%\jre
CLASSPATH : %JAVA_HOME%\lib;%JAVA_HOME%\jre\lib
PATH : other-entries;%JAVA_HOME%\bin
```

*Make sure that `PATH` doesn't contain references to another Java installation directory.*

### 3. Download [Android SDK](https://developer.android.com/studio/index.html).

Go to the bottom of the website and find *Get just the command line tools* section. We don't need Android Studio here. Choose command line tools like on the image below:

![Android SDK](/assets/images/2017/android/sdk.png)

Unzip this to desired SDK location.

### 4. Install SDK components

Now we need to install Android components. We are not using Android Studio so we will need to run console.

To install those things we will use console tool called 'sdkmanager.bat'. It is inside `\tools\bin\` directory of `[Your AndroidSDK location]` — in my example it was directly in custom folder on `C:` drive.

If you would like to check newest packages versions simply run `sdkmanager.bat --list` command.
To run scripts in `*.bat` you need to enter command line. To do this get into `[AndroidSDK]\tools\bin\` and in directory bar write `cmd` like on gif below:

![cmd gif](/assets/images/2017/android/cmd.gif)

_Don't rely on versions below — those was newest while I was writing this tutorial._

Install required packages like this:
```
sdkmanager.bat platforms;android-27
sdkmanager.bat platform-tools
sdkmanager.bat build-tools;27.0.1
sdkmanager.bat extras;google;usb_driver
```
### 6. Setup locations in Unity

Go to `Edit/Preferences/External tools` and setup paths according to locations you have choosen:

![Unity settings](/assets/images/2017/android/unity.png)

### 6. That's it. Now you can proceed with steps from [Unity documentation](https://docs.unity3d.com/Manual/android-sdksetup.html). From third step or so.

## ... a few steps further. You are ready to become Unity Android Developer! Create some android games or plugins? Good luck!
---
excerpt: "How to set up Unity for Android development? How to download and install JDK, set Android SDK PATH and other Android stuff on Windows? Here you have step by step receipt to download & start Android development environment for Unity."
header:
  overlay_image: /assets/images/2017/android/cover.png
  overlay_color: "#333"
  overlay_filter: 0.5

title: "Configure Android SDK for Unity"
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

That's it. Now you can proceed with steps from [Unity documentation](https://docs.unity3d.com/Manual/android-sdksetup.html). From third step or so.

... a few steps further. You are ready to become Unity Android Developer! Take a look below for even better start.


## Done with tutorial? I've prepared some book recomendations for you!

#### [Learning C# by Developing Games with Unity 2019: Code in C# and build 3D games with Unity, 4th Edition](https://www.amazon.com/gp/product/1789532051/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1789532051&linkCode=as2&tag=koprowski05-20&linkId=1c6d3fefea54bbcee3b5b9e0e89fb04b)
> The book caters to developers and programmers who want to get started with C# programming in a fun and engaging manner. Anyone who wants to build games and script in C# language and Unity can take this book up. No prior programming or Unity experience is required.

[![Learning C# by Developing Games with Unity 2019](https://images-na.ssl-images-amazon.com/images/I/51RqggaQarL.jpg)](https://www.amazon.com/gp/product/1789532051/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=1789532051&linkCode=as2&tag=koprowski05-20&linkId=1c6d3fefea54bbcee3b5b9e0e89fb04b)


#### [Reality Is Broken: Why Games Make Us Better and How They Can Change the World](https://www.amazon.com/gp/product/0143120611/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=0143120611&linkCode=as2&tag=koprowski05-20&linkId=13b9aaecdacfaaf16ebe293e8f3e4334)

**Must read for game developer! - this book will tell you why this job is so important**
> The book did a superb job of outlining concrete examples of why we like games in the first place, and how we can transform that interest into something that will make our lives and the lives of others better. - Michael Andersen on [ARGNet](http://www.argn.com/2011/01/a_commentary_on_jane_mcgonigals_new_book_reality_is_broken/)

[![Reality Is Broken](https://images-na.ssl-images-amazon.com/images/I/518%2Bt9RNR5L._SX324_BO1,204,203,200_.jpg)(https://www.amazon.com/gp/product/0143120611/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=0143120611&linkCode=as2&tag=koprowski05-20&linkId=13b9aaecdacfaaf16ebe293e8f3e4334)


#### [Unity in Action: Multiplatform Game Development in C# with Unity 5](https://www.amazon.com/gp/product/161729232X/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=161729232X&linkCode=as2&tag=koprowski05-20&linkId=4dd5d011e0a3e8ff96ff46e5236ad31a)
> This is a book about programming games in Unity. Think of it as an intro to Unity for experienced programmers. The goal of this book is straightforward: to take people who have some programming experience but no experience with Unity and teach them how to develop a game using Unity. 

[![Unity in Action: Multiplatform Game Development in C# with Unity 5](https://images-na.ssl-images-amazon.com/images/I/510Qt3luBQL._SX396_BO1,204,203,200_.jpg)](https://www.amazon.com/gp/product/161729232X/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=161729232X&linkCode=as2&tag=koprowski05-20&linkId=4dd5d011e0a3e8ff96ff46e5236ad31a)

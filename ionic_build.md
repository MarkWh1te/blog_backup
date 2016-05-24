# Use Inoic Build Android App

[Ionic Official Guide](http://ionicframework.com/docs/guide/installation.html)

### 1. Install JDK 

open your termial
>sudo apt-get install openjdk-7-jre

### 2. Install Android SDK  
[Cordova Official Guide](http://cordova.apache.org/docs/en/3.4.0/guide/platforms/android/index.html#Android%20Platform%20Guide)


* Download android SDK

__Android SDK means Android software development kit.It includes a comprehensive set of development tools.__

[What is SDK?](https://en.wikipedia.org/wiki/Software_development_kit)

[Android software development](https://en.wikipedia.org/wiki/Android_software_development)

[linux android Sdk Download Link](https://dl.google.com/android/android-sdk_r24.4.1-linux.tgz) 

* Add  

>vim  ~/.bashrc

add these lines
>export $ANDROID_HOME=/path/to/your/android-sdk-linux

>export PATH=$ANDROID_HOME/tools:$PATH

>export PATH=$ANDROID_HOME/platform-tools:$PATH


now open your termial 
>android 

__install these packages__:

Android SDK Build Tools

Android SDK Platform-tools

Android SDK Tools

Android Support Repository

Google Repository


### 3. Install Ionic
>sudo npm install -g cordova

>sudo npm install -g ionic

>cd myapp

>ionic platform add android

>cd myapp

>ionic serve

you will your project on web brower

### 4. Testing 

* Install adb 

Android Debug Bridge (adb) is a versatile command line tool that lets you communicate with an emulator instance or connected Android-powered device.

[What is adb?](https://developer.android.com/studio/command-line/adb.html)

open your termial
>sudo add-apt-repository ppa:nilarimogard/webupd8

>sudo apt-get update

>sudo apt-get install android-tools-adb android-tools-fastboot



Remember you need __enable Developer Options on your Android phone__ and link it with your PC.

>cd /way/to/your/android/sdk/Android/Sdk/platform-tools

>adb devices

>adb start-server 

>cd myapp

>ionic run android

### 5. Publishing
>cd myapp

>ionic build android

### 6. Publishing with Corsswalk
>cd myapp

>ionic browser add crosswalk

>vim platform/android/build-extras.gradle

add this line 
>cdvBuildMultipleApks=false

save 

>ionic run android







 
 
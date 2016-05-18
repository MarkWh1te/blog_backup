# Use Inoic Build Android App

## Installation
http://ionicframework.com/docs/guide/installation.html
### 1. Install JDK 
http://askubuntu.com/questions/48468/how-do-i-install-java
### 2. Install Android SDK  
http://cordova.apache.org/docs/en/3.4.0/guide/platforms/android/index.html#Android%20Platform%20Guide
### 3. Install Ionic
>sudo npm install -g cordova

>sudo npm install -g ionic

>cd myapp

>ionic platform add android

under /root/of/ionic/project
### 4. Testing 
on browser
>cd myapp
>ionic serve

on phone
>cd /way/to/your/android/sdk/Android/Sdk/platform-tools

>adb devices

>adb start-server 

>cd myapp

>ionic run android

### 5. Publishing
>cd myapp

>ionic build android

### 5. Publishing with Corsswalk
>cd myapp

>ionic browser add crosswalk

>vim platform/android/build-extras.gradle

add this line 
>cdvBuildMultipleApks=false

save 

>ionic run android







 
 
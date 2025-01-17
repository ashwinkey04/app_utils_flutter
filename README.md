# App Utils
  
[![Pub Package](https://img.shields.io/badge/pub-v0.4-blue)](https://pub.dartlang.org/packages/app_utils)
[![Pub Package](https://img.shields.io/badge/Licensce%20-MIT-green)](https://opensource.org/licenses/MIT)



  Application  plugin which provides utility functions for
  Android and iOS.
 
## Installation

###  Android
 
In android you can either declare QUERY_ALL_PACKAGES permission (to provide broader app package visibility) or can declare packages inside <queries> 
tag in you AndroidManifest.xml file.

  Note -> Using QUERY_ALL_PACKAGES permission may cause your app to be rejected on playstore if your app doesn't have any core functional which is     
          required broad package visibility (eg antivirus app that needs limit visibility to scan all apps in your device). If your app does not require           QUERY_ALL_PACKAGES permission as a core functionality in your app, consider using the <queries> tag.
  
  
    
    <uses-permission android:name="android.permission.QUERY_ALL_PACKAGES"/>
     
    OR
    
    <queries>
     <package android:name="com.whatsapp.businessapp"/> 
     <package android:name="in.techbyvishesh.myapp"/>
    </queries>   

###  iOS

In Ios, for opening the target app from your app, you need to provide the URL scheme of the target app.

To know more about URLScheme in iOS, please visit below link. <br> https://developer.apple.com/documentation/xcode/defining-a-custom-url-scheme-for-your-app

In your deployment target is greater than or equal to 9 then also need to update another app information in your Info.plist.

    <key>LSApplicationQueriesSchemes</key>
    <array>
    <string>whatsapp</string> // url scheme
    </array>

<br>
<img src="https://i.ibb.co/ZH3D7nP/ezgif-com-gif-maker.gif" height="500" width="300">


## List of supported functions
1. <b>launchApp (Android and iOS)</b> : <br>   It opens target application from provided package name in Android and URLScheme in iOS.
<br>
<br>   
2. <b>getInstalledApps (Android)</b> : <br>
    It returns a list of the installed applications from your devices.
<br>
<br>
3. <b>canLaunchApp (Android & iOS)</b> : <br> It checks application is launchable or not.
   <br>
   <br>
4. <b>getCurrentDeviceInfo (Android and iOS)</b> : <br> It returns current device information.
   <br>
   <br>
5. <b>getCurrentAppInfo (Android and iOS)</b> : <br> 
    It returns your application information.
<br>
<br>   
6. <b>readLaunchedData (Android and iOS)</b> : <br>
    It allows us to read sender application data. In android, it reads data from activity intent but in iOS, it reads data from URL Scheme.
   <br>
   <br>
7. <b>openDeviceSettings (Android and iOS)</b> : <br>
   - It allows us to open settings page from your application.<br>
   - In Android, it supports multiple settings option.<br>
   - In iOS, due to apple restriction, it only supports the main settings page.For more info, please 
     <a href="https://developer.apple.com/forums/thread/100471">visit here</a>.
   

## Upcoming features

1. <b>requestDeviceAuth</b> : Open the device unlock screen on Android and iOS.
2. <b>playAudio</b>: Allows you to play audio on your device.
3. <b>openDeviceSensor</b>:  Allows you to open device sensors.


## Bugs or Requests
If you encounter any problems feel free to open an issue. 
If you feel the library is missing a feature, please raise a ticket on <a href ="https://github.com/vishesh005/app_utils/issues">
GitHub</a> and I'll look into it. Pull request are also welcome.





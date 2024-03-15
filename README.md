# Web to Android Mobile App

## This is MiracleWebView application with Advance functionalities

# Screenshots
![ANDROID WEBVIEW](https://imgur.com/5Ngr8E7.jpeg)

# Configurations

## Change Package name

- Change package name in  ```android/app/build.gradle```

```json
defaultConfig {
    applicationId "com.miracle.webmobile"
    ...
}
```

- Replace with your package name

```json
defaultConfig {
    applicationId "your.package.name"
    ...
}
```

## Replace Logo
- Replace logo **logo.png** in ```android/app/src/main/res/drawable/``` directory

## Website URL
- Change url variable in ```android/app/src/main/java/com/miracle/webmobile/MainActivity.kt```
```dart
String MAIN_URL = "https://www.theandroid-mania.com/";
```

## App Credentials
- Change App Name  ```android/app/src/main/res/values/strings.xml```
```xml
<string name="app_name">Web Mobile App</string>
```

## Push Notifications

- First thing you need to do is go to **(https://firebase.google.com/)** and make an account to gain access to their console. After you gain access to the console you can start by creating your first project.
  ![FIREBASE NEW PROJECTS](https://imgur.com/SwpWqod.png)

- Give the package name of your project (mine is **com.miracle.webmobile**) in which you are going to integrate the Firebase. Here the **google-services.json** file will be downloaded when you press add app button.
  ![FIREBASE ADD JSON](https://imgur.com/yycT5G4.png)

- Project Overview in open Project Settings.
  ![FIREBASE SETTING](https://imgur.com/WMSSdPg.png)

- Open services Account and click Generate new private key then Generate Key.
  ![FIREBASE GENERATE KEY](https://imgur.com/oGCuvoh.png)

- Paste the downloaded json file under Service Account json in Onesignal.
  ![ONESIGNAL ADD](https://imgur.com/pENV0Ux.png)

- Copy your App ID and `lib/main.dart` paste ID in `String ONESIGNAL_ID = "########-####-####-####-############";`.
  ![ONESIGNAL SET APP ID](https://imgur.com/LRhKDlm.png)

## How to add Onesignal
- Copy your App ID and `lib/main.dart` paste ID in `String ONESIGNAL_ID = "########-####-####-####-############";`.
```dart
OneSignal.Debug.setLogLevel(OSLogLevel.verbose);
OneSignal.initialize(ONESIGNAL_ID);
OneSignal.Notifications.requestPermission(true);
```

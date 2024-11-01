# Photo Viewer

> This plugin is intended to show a picture from an URL into a Photo Viewer with zoom features.
>
> This version (1.2.8) has been tested with Cordova 12.0.1



## How to Install

Cordova:

```bash
cordova plugin add https://github.com/remoorejr/cordova-plugin-photoviewer.git
```

### Android

> Tested with Cordova Android 13.0.0 API Levels 25 through 34

### iOS

> Tested with Cordova iOS 7.1.1, Xcode 15.2, iOS 17.0

### API

#### Show an image

```
PhotoViewer.show('http://my_site.com/my_image.jpg', 'Optional Title');
```

You have to pass as third parameter the following options as object.

Options:

- share: boolean - Option is used to hide and show the share option.
- closeBtn: boolean - Option for close button visibility when share false [ONLY FOR iOS]
- copyToReference: boolean - If you need to copy image to reference before show then set it true [ONLY FOR iOS]
- headers: string - HTTP Headers [MUST BE PROVIDED]
- picassoOptions: object - Options for picasso dependency [ONLY FOR ANDROID]

##### Usage

```

default piccasoOptions: {
            fit: true,
            centerInside: true,
            centerCrop: false
        }

var options = {
    share: true,            // default is false
    closeButton: false,     // default is true
    copyToReference: true,  // default is false
    headers: '',            //  iOS: If this is not provided, an exception will be triggered
    piccasoOptions: { }     //  ANDROID: If this is not provided, defaults will be used
};



PhotoViewer.show('http://my_site.com/my_image.jpg', 'Optional Title', options);
```

### Versions

(1.0.2) Removed Podfile and the dependency  
(1.1.0)

- Removing project dependencies.
- Moving to Gradle
- Adding Square's Picasso as Image Loader
- New Optional Title
- Share button and title bar
- Automatic close on error.
- Support for content:// Uris from Cordova
- Replaced old namespace
- Published to NPM

(1.1.1)

- Fix for sharing due to online restriction

(1.1.2)

- Fix issues on iOS
- iOS title not updating

(1.1.3)

- Issue fixes

(1.1.4)

- Base64 Support on Android

(1.1.5)

- Option to hide and show share button on Android

(1.1.7)

- Fix OOM issues on Android

(1.1.9/10)

- Fix how image is shown on Android

(1.1.17)

- Additional options added for iOS
- Fix share issue with SDK version 24 or above on Android

(1.1.9)

- Support for Headers
- Enable or Disable Picasso Options ( Only Android ): fit, centerInside, centerCrop.

(1.1.21)

- Fix Typo in PhotoViewer.js
- Fix Typo in PhotoActivity.java

(1.1.22)

- Ask always for permissions on Android.

(1.2.0)

- Adding TS files from next version to support TypeScript projects

(1.2.1)

- Native fixes on Android platform

(1.2.2)

- PRs: #164 #165 #167

(1.2.3)

- PRs: #179

(1.2.4)

- Removing Source Maps because of errors

(1.2.5)

- Update Picasso Library to 2.71828
- Fixed Picasso Bug
- Thanks to @TdoubleG

(1.26)

- Modified gradle build file to support Android 12
- @remoorejr

(1.28)

- removed permission checks, READ and WRITE EXTERNAL for Android API Level 30+, not required 
- removed media read permission request, Android 12 plus, not required and is flagged on GPS submission
- @remoorejr

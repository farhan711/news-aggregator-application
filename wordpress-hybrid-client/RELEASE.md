# Release

Male sure you have ios and/or android platforms installed. If you have correctly ran ```npm run installCordova``` it should be fine otherwise go back to [BUILD.md](BUILD.md).

## Android

### Get and save licence key

<https://support.google.com/googleplay/android-developer/answer/186113?hl=en>

Copy and past the key within your ```~/.ssh``` folder with that name ```android_wphc.keystore```

NB: You can put the key wherever you want and even give it another name but if you do that, you will need to modify ```release.sh``` accordingly.

### Keyboard adjustement

Open ```platforms/android/AndroidManifest.xml``` and change ```android:windowSoftInputMode="adjustResize"``` into ```android:windowSoftInputMode="adjustNothing"``` it will prevent screen hiccup when searching.

### Build PROD APKs

```
npm run build
```

Then answer to the prompt.

## iOS

### Documentation

<https://developer.apple.com/programs/ios/gettingstarted/>

<https://developer.apple.com/library/mac/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Chapters/CreatingiTunesConnectRecord.html#//apple_ref/doc/uid/TP40011225-CH13>

<http://codewithchris.com/submit-your-app-to-the-app-store/>

### Install sigh

Sigh allow to sign .app with a provisioning file via the terminal

```
# https://github.com/KrauseFx/sigh
sudo gem install sigh
```

### Build PROD IPA

```
npm run build
```

Then answer to the prompt.

### Use XCode or Application Loader

Once the IPA is signed, all you need to do is sending the package to Apple for review.

### Frequent errors

#### Submitting iOS app to app store application identifier invalid

<http://stackoverflow.com/questions/20120128/submitting-ios-app-to-app-store-application-identifier-invalid>

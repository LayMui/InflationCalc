# Instructions
1. npx react-native init InflationCalc (refer to https://reactnative.dev/)
2. cd InflationCalc
3. cd ios
4. pod install
5. In xcode, open InflationCalc.xcworkspace and build to make sure it can build successfully.

6. npm install appcenter appcenter-analytics appcenter-crashes --save-exact
7. Open the InflationCalc.xcworkspace in xcode
8. Create a new file AppCenter-Config.plist 
    Right click to Create file Go to Resource section and select PropertyList
    Add the content
    <dict>
    <key>AppSecret</App>
    <string><Copy and paste from AppCenter Copy Secret of the app></Copy></string>
  </dict>

  9. https://appcenter.ms/orgs/LayMuiQA_testing/apps/InflationCalc
  Go to AppDelegate.m
  Add 
    #import <AppCenterReactNativeShared/AppCenterReactNativeShared.h>
    #import <AppCenterReactNative.h>
    #import <AppCenterReactNativeAnalytics.h>
    #import <AppCenterReactNativeCrashes.h>

    Add these lines to the didFinishLaunchingWithOptions method before the 
    return YES;

    [AppCenterReactNative register];
    [AppCenterReactNativeAnalytics registerWithInitiallyEnabled:true];
    [AppCenterReactNativeCrashes registerWithAutomaticProcessing];


```
gem uninstall cocoapods
gem uninstall cocoapods-core
gem uninstall cocoapods-downloader
gem install cocoapods
```


# Steps: 
```
sudo xcodebuild -license
rvm reinstall 2.6.6
sudo gem install cocoapods
pod --version
```

  
  
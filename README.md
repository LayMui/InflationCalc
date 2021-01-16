# Instructions
1. npx react-native init InflationCalc (refer to https://reactnative.dev/)
2. cd InflationCalc
3. cd ios
4. pod install
5. In xcode, open InflationCalc.xcworkspace and build to make sure it can build successfully.

6. npm install appcenter appcenter-analytics appcenter-crashes --save-exact

6a. cd ios and run pod install --repo-update to install cocoapods dependencies

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

On android
```
go to main
create a folder called assets
and under assets, create a file called appcenter-config.json
with the content
{
    "app_secret" : "xxxx"
}
Navigate to App center and copy the app secret for android app
Go to res folder
Go to values folder
and open strings.xml
add the following:
<string name="appCenterCrashes_whenToSendCrashes"
            moduleConfig="true"
            translatable="false">ALWAYS_SEND</string>
<string name="appCenterAnalytics_whenToEnableAnalytics"
    moduleConfig="true"
    translatable="false">ALWAYS_SEND</string>
```

[![Build status](https://build.appcenter.ms/v0.1/apps/d822311b-92cc-475e-99fe-9d4d0953783d/branches/dev/badge)](https://appcenter.ms)
  
[![Build status](https://build.appcenter.ms/v0.1/apps/ee8ea782-fd20-42d0-a87b-a7d5770e2a0d/branches/dev/badge)](https://appcenter.ms)


[![Build status](https://build.appcenter.ms/v0.1/apps/a4e334ca-baf9-4507-8b9f-2b7de73e9df7/branches/dev/badge)](https://appcenter.ms)
[![Build status](https://build.appcenter.ms/v0.1/apps/f5278098-f754-429c-a22f-e15dfe9079bd/branches/feature2/badge)](https://appcenter.ms)

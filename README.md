# bugsnag-react-native
Clean react native project to demonstrate an issue with the latest version of Bugsnag.

```
npx react-native init BugsnagReactNative --version 0.61.5
yarn add bugsnag-react-native
cd ios
pod install
```

Import Bugsnag.h in the AppDelegate.m:

```
#import <BugsnagReactNative/Bugsnag.h>
```

Try to compile and you'll get an error as Bugsnag.h is importing a private header file - BugsnagPlugin.h: https://github.com/smacgregor/bugsnag-react-native/blob/master/ios/BugsnagReactNative/AppDelegate.m#L15

<img width="917" alt="Screen Shot 2020-03-31 at 5 23 19 PM" src="https://user-images.githubusercontent.com/1521460/78087095-c19e5080-7374-11ea-807a-b5d7b3adec76.png">


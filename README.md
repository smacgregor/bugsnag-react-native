# bugsnag-react-native
Clean react native project to demonstrate an issue with the latest version of Bugsnag.

```
npx react-native init BugsnagReactNative --version 0.61.5
yarn add bugsnag-react-native
```

Import Bugsnag.h in the AppDelegate.m:

```
#import <BugsnagReactNative/Bugsnag.h>
```

Try to compile and you'll get an error as Bugsnag.h is importing a private header file - BugsnagPlugin.h.

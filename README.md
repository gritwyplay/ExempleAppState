# ExempleAppState

Dummy project to demonstrate an strange behavior regarding react-native AppState module.

## Output of `npx react-native info`

info Fetching system and libraries information...
System:
    OS: Linux 5.19 Arch Linux
    CPU: (6) x64 Intel(R) Core(TM) i5-8500 CPU @ 3.00GHz
    Memory: 7.20 GB / 15.43 GB
    Shell: 5.9 - /usr/bin/zsh
  Binaries:
    Node: 18.8.0 - /usr/bin/node
    Yarn: 1.22.19 - /usr/bin/yarn
    npm: 8.19.1 - /usr/bin/npm
    Watchman: Not Found
  SDKs:
    Android SDK:
      API Levels: 30, 31, 33
      Build Tools: 29.0.0, 29.0.2, 30.0.3, 31.0.0, 33.0.0
      System Images: android-30 | Android TV Intel x86 Atom, android-30 | Google TV Intel x86 Atom
      Android NDK: 25.1.8937393
  IDEs:
    Android Studio: AI-212.5712.43.2112.8815526
  Languages:
    Java: 1.8.0_345 - /usr/bin/javac
  npmPackages:
    @react-native-community/cli: Not Found
    react: 18.0.0 => 18.0.0 
    react-native: 0.69.5 => 0.69.5 
  npmGlobalPackages:
    *react-native*: Not Found
info React Native v0.70.0 is now available (your project is running on v0.69.5).
info Changelog: https://github.com/facebook/react-native/releases/tag/v0.70.0.
info Diff: https://react-native-community.github.io/upgrade-helper/?from=0.69.5.
info To upgrade, run "react-native upgrade".


## Steps to reproduce

1. Start the demo app (https://github.com/gritwyplay/ExempleAppState)
2. Send an intent ( `adb shell am start -a "android.intent.action.VIEW" -d test://test`)
3. Observe current app state in the app ("Current state is: xxxxxx")

### Expected

1. The App start
2. The intent is fired
3. The current state stay active

### Actual

1. As Expected
2. As Expected
3. The current state quickly change to "background" before come back to "active"




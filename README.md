# ExempleAppState

Dummy project to demonstrate an strange behavior regarding react-native AppState module.

## Output of `npx react-native info`
```
info Fetching system and libraries information...
System:
    OS: Linux 5.19 Arch Linux
    CPU: (6) x64 Intel(R) Core(TM) i5-8500 CPU @ 3.00GHz
    Memory: 3.94 GB / 15.43 GB
    Shell: 5.9 - /usr/bin/zsh
  Binaries:
    Node: 18.8.0 - /usr/bin/node
    Yarn: 1.22.19 - /usr/bin/yarn
    npm: 8.19.1 - /usr/bin/npm
    Watchman: Not Found
  SDKs:
    Android SDK:
      Android NDK: 25.1.8937393
  IDEs:
    Android Studio: AI-212.5712.43.2112.8815526
  Languages:
    Java: Not Found
  npmPackages:
    @react-native-community/cli: Not Found
    react: 18.1.0 => 18.1.0 
    react-native: 0.70.0 => 0.70.0 
  npmGlobalPackages:
    *react-native*: Not Found

```

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




# FirebaseAirshipConflictExample

Copyright (c) 2022-2023, Media.Monks.

This is to demonstrate how [Firebase](https://github.com/dpa99c/cordova-plugin-firebasex) and
[Airship](https://github.com/urbanairship/urbanairship-cordova) plug-ins conflict in a Cordova app on iOS: even though
`FIREBASE_FCM_AUTOINIT_ENABLED` variable is set to `false` for Firebase the plug-in still sets its delegate for
`UNUserNotificationCenter` preventing regular flow of notifications for Airship.

We've patched the above Firebase plug-in in [our fork](https://github.com/mediamonks/cordova-plugin-firebasex) to support iOS-specific variable `IOS_FCM_ENABLED` that can be set to `false` to completely disable FCM-related features.

To try out the fork:

```
cordova -d plugin rm cordova-plugin-firebasex
cordova -d plugin add github:mediamonks/cordova-plugin-firebasex --variable IOS_FCM_ENABLED=false
```

A similar issue for Android can be worked around by changes in `config.xml` as shown in this example.

(Note that the example uses API keys of our test Firebase and Airship projects. These were created just for this
example, so keeping the keys in the repo is not an issue.)

---

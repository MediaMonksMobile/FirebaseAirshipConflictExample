# FirebaseAirshipConflictExample

Copyright (c) 2022, Media.Monks.

This is to demonstrate how [Firebase](https://github.com/dpa99c/cordova-plugin-firebasex) and
[Airship](https://github.com/urbanairship/urbanairship-cordova) plug-ins conflict in a Cordova app: even though
`FIREBASE_FCM_AUTOINIT_ENABLED` variable is set to `false` for Firebase the plug-in still sets its delegate for
`UNUserNotificationCenter` preventing regular flow of notifications for Airship.

Note that the example uses API keys of our test Firebase and Airship projects. These were created just for this
example, so keeping the keys in the repo is not an issue.

---

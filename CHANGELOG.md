## [0.0.1]

*  Initial release

## [0.0.2]

* README fixes

## [0.0.3]

* Fix changelog


## [0.0.4]

* Updated README

## [0.0.5]

* Updates to iOS code to support both legacy notifications via UILocalNotification (before iOS 10) and the User Notifications framework introduced in iOS 10

## [0.0.6]

* Add ability to customise the presentation options when a notification is triggered while the app is in the foreground for iOS notifications presented using the User Notifications Framework (iOS 10+). IMPORTANT: the named parameters for iOS initialisation settings constructor have had to change to differentiate between permission options and presentation options

## [0.0.7]

* Fix notifications on Android so tapping on them will remove them and will also start the app if it has been terminated.

## [0.0.8]

* Enable ability to customise sound and vibration for Android notifications.

## [0.0.9]

* Enable ability to customise the sound for iOS notifications (**IMPORTANT** requires testing on older iOS versions < 10). Can now specify default presentation options for iOS (**BREAKING CHANGE** named parameters for iOS initialisation have changed) that can also be overridden at the notification level). Fixes for reading in specified options in iOS.

## [0.1.0]

* Add support for big text style for Android notifications and format the big text style specific content using HTML markup.

## [0.1.1]

* Add ability to use HTML markup to format the title and content of Android notifications


## [0.1.2]

* Bug fix in calculating when to show a scheduled Android notification. Ensure scheduled Android notifications will remain scheduled even after rebooting.

## [0.1.3]
* Fix broken example app for iOS due to incorrect reference to custom sound file. Added ability to handle when a notification is tapped. See updated example for details on how to do this and will navigate to another page. Note that the second page isn't rendering full-screen on Android if the notification was tapped on while the app was in the foreground. Suspect that this is Flutter rendering issue and have logged this on the Flutter repository at https://github.com/flutter/flutter/issues/16636

## [0.1.4]
* Add inbox notification style

## [0.1.5]
* **BREAKING CHANGES** There are no functional changes. This is an API cleanup release where I've reorganised the Dart classes to better separate them by platform. What this means is that the import statements in your coode will need to be fixed. Apologies to anyone using the plugin but I feel that this was necessary as Flutter may target additional platforms in the future. Hopefully you'll agree that the end result looks a better :)

## [0.1.6]
* **BREAKING CHANGES** Apologies again, this is another cleanup release. FlutterLocalNotifications class has been renamed to FlutterLocalNotificationsPlugin now as it makes more sense from a readability perspective. More importantly, the class and methods are also no longer static to faciliate mocking and testing. It's something I should've picked up on earlier so sorry once again. Check the source code for an example on how to mock the plugin when testing

## [0.1.7]
* Add ability to show grouped notifications on Android. Example code has been updated to demonstrate this functionality.
* Fixed the example project so it works with the new release of Cocoapods (1.5.0)
* Fixes for when API methods were called without specifying platform specific settings
# Android-Core-SDK-v1.18

Release candidate v1.18 released 24/Apr/2016.

This new version exposed 3 new delegate methods:

/**
* By default the chat\survey window is hide when the visitor is tapping on the chat\survey background.
* In order to prevent background tapping from hiding the chat\survey set this callback to false
* @return - Set to false if you would like keep the chat\survey open even when the visitor tapping on the background.
* In this case the chat\survey will be hide only base on back or cancel button.
* Default: true
*/
public boolean shouldHideLPWindowOnBackgroundTapping();


/**
* Indicate that an custom notification need to replace the default notification that issue by the SDK for chat events.
* @return - Set to true if you would like override the default SDK chat notifications.
* Default: false
*/
public boolean shouldUseCustomNotification();

/**
* Replacing the SDK notification with custom notification that issue by the app.
* Allow the app full control on the chat notification that should be issue by the SDK
*
* If shouldUseCustomNotification return true - you have to implement this method or chat notifications will not be issue.
* @param title - notification title
* @param message - notification message
*/
public void showCustomNotification(String title, String message);


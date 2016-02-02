# Android-Core-SDK-v1.16

Release candidate v1.16 released 2/2/2016.

New version contains bug fixes and ability to configure timeout when app enters onPause().

In order to update the timeout the app will need to use the constructor ApplicationLifecycleHandler(this, 300) in the application object.

The second parameter (300) is optional and use to define delay time in ms that use when we check if the app moved to background. 

Default = 150ms; Min = 50ms; Max = 2000ms. 

Example:

if (android.os.Build.VERSION.SDK_INT >= Build.VERSION_CODES.ICE_CREAM_SANDWICH) {
    registerActivityLifecycleCallbacks(new ApplicationLifecycleHandler(this, 300));
}

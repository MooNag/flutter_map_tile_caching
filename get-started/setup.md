# Additional Setup

## Background Downloading

This extra setup is only required if you plan to use the background bulk downloading functionality.

### Android

Add the following to 'android\app\src\main\AndroidManifest.xml' and any other manifests:

```diff
 <manifest xmlns:android="http://schemas.android.com/apk/res/android" package="packageName">
+    <uses-permission android:name="android.permission.FOREGROUND_SERVICE" />
+    <uses-permission android:name="android.permission.WAKE_LOCK" />
+    <uses-permission android:name="android.permission.REQUEST_IGNORE_BATTERY_OPTIMIZATIONS"/>
 <application android:label="appName" android:icon="appIcon">
```

This will allow the application to acquire the necessary permissions (should the user allow them at runtime) to a background process.

* `FOREGROUND_SERVICE`: allows the application to start a foreground service - a type of Android service that can run in the background, as long as the application isn't force stopped.
* `WAKE_LOCK`: allows the background process (technically foreground service) to run even when the device is locked/asleep. Also allows the acquisition of a WiFi lock.
* `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` (must be requested at runtime): assists with the background process not being killed by the system.

### Other Operating Systems

Background downloading is unfortunately not supported on any other platforms, due to dependency limitations, and thus limitations of the respective platform.

PRs to add this functionality are welcome!

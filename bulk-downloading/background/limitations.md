# Limitations

## Android Only Support

Unfortunately, background downloading is available on Android only, due to the strict limitations imposed by iOS. This is unlikely to change in the future, especially as I am currently unable to develop for iOS.

## Background Processes

There is some confusion about the way background process handling works on Android, so let me clear it up for you: it is confusing.

Each vendor (eg. Samsung, Huawei, Motorola) has their own methods of handling background processes.

Some manage it by providing the bare minimum user-end management, resulting in process that drain battery because they can't be stopped easily; others manage it by altogether banning/strictly limiting background processes, resulting in weird problems and buggy apps; many manage it by some layer of control on top of Android's original controls, making things more confusing for everyone.&#x20;

Therefore there is no guaranteed behaviour when using this functionality. You can see how many vendors will treat background processes here: [dontkillmyapp.com](https://dontkillmyapp.com/); you may wish to link your users to this site so they can properly configure your app to run in the background.

To try and help your users get to the right settings quicker, use the `requestIgnoreBatteryOptimizations()` method before starting a background download. This will interrupt the app with either a dialog or a settings page where they can opt-in to reduced throttling. There is no guarantee that this will work, but it should help: this is not required and the background download will still _try_ to run even if the user denies the permissions.

Internally, a foreground service is actually used. This allows the service to run as long as the app hasn't been force stopped.

## Recovery Effectiveness

The effectiveness of the [recovery.md](../../usage/roots-and-stores/recovery.md "mention") is reduced by background downloading.

If the user leaves the application, then the recovery system may report the ongoing background download as failed, as it has no way of knowing about it. If the user tries to retry the download, both downloads may then fail, and the recovery system may fail also.

There is no way of resolving this situation. You may prefer to disable recovery on background downloads all together.

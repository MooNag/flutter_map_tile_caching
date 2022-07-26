# Example Application

This package contains a full example application - prebuilt for Android and Windows - showcasing the most important features of this package.

Feel free to use the app as a starting point for your application, it contains some useful UI patterns.

{% hint style="danger" %}
By using the example application, you must comply to your tile server's ToS.

OpenStreetMap's (the default throughout the application) can be [found here](https://operations.osmfoundation.org/policies/tiles). If you cannot comply to these rules, you should find one that you can comply to and get the appropriate source URL (which can be customised in the application).
{% endhint %}

## Prebuilt Example Applications

{% embed url="https://drive.google.com/drive/folders/1hBYYaZVUYgXyCEinARLuOE8SAIaV94kM" %}
Prebuilt Example Applications (Google Drive Listing)
{% endembed %}

## Installation Guides

### Android

To run the prebuilt Android application on most devices, download the appropriate .apk package (from [#prebuilt-example-applications](example-application.md#prebuilt-example-applications "mention")) to your device, then execute it to install it.

To install the app, execute the file. After installation, it will appear in the launcher like any other application.

{% hint style="info" %}
The operating system may request permissions to install applications from unknown sources: you must allow this.
{% endhint %}

### Windows

To run the prebuilt Windows application, download the appropriate .zip archive (from [#prebuilt-example-applications](example-application.md#prebuilt-example-applications "mention")) and extract it to a suitable location on your system.

Then run the 'example.exe' program it contains: it does not require any installation.

{% hint style="info" %}
You may receive security warnings depending on your system setup: these are false positives.
{% endhint %}

### Other Platforms

For other platforms, there are no prebuilt applications.

You'll [clone this project](https://github.com/JaffaKetchup/flutter\_map\_tile\_caching.git), open the 'example' directory, and then build for your desired platform using Dart and Flutter as normal.

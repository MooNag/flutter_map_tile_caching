---
description: Applies only to Roots
---

# Recovery

```dart
FlutterMapTileCaching.instance.rootDirectory.recovery;
```

The recovery system is designed to rescue failed bulk downloads, in the event of an unexpected error - such as a fatal crash or other external event.

{% hint style="warning" %}
You should not rely on the recovery system to be 100% reliable, even though it is built to be as close to that as possible.
{% endhint %}

## Available APIs

| API                      | Explanation                                                            |
| ------------------------ | ---------------------------------------------------------------------- |
| `recoverableRegions`     | Get a list of all recoverable regions, not just those that have failed |
| `failedRegions`          | Get a list of recoverable regions that have failed                     |
| `getRecoverableRegion()` | Get a specific region from the recoverable list                        |
| `getFailedRegion()`      | Get a specific region from the failed list                             |
| `cancel()`               | Safely cancel/remove a recoverable region                              |

## ID System

Recoverable regions are identified internally by an `int` ID number. All the methods above make use of this ID number, and so (to ensure continuity) the `RootRecovery` object returned is internally a singleton.

This number is generated using the following algorithm, which hopefully ensures a unique number:

```dart
hashValues(
    region, // Hash code for the `DownloadableRegion`
    tileProviderSettings, // Hash code for the current tile provider settings
    _storeDirectory.getTileProvider(tileProviderSettings), // Hash code for an instance of the store directory's `TileProvider`
) * DateTime.now().millisecondsSinceEpoch;
```

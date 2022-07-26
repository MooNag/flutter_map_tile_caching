# 3⃣ Start In Foreground

{% hint style="danger" %}
You must comply to your tile server's ToS. Failure to do so may result in you being banned from their services.

OpenStreetMap's can be [found here](https://operations.osmfoundation.org/policies/tiles): specifically bulk downloading is discouraged, and forbidden after zoom level 13. Other servers may have different terms.

This package is not responsible for your misuse of another tile server.
{% endhint %}

```dart
FMTC.instance('storeName').download.startForeground();
```

## Available Parameters

| Parameter              | Type                                                                              | Explanation                                            | Default                                                           |
| ---------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------ | ----------------------------------------------------------------- |
| `region`               | ``[`DownloadableRegion`](prepare.md)``                                            | The actual region to download                          | _required_                                                        |
| `tileProviderSettings` | ``[`FMTCTileProviderSettings?`](../usage/integration.md#tile-provider-settings)`` | Settings for the downloader tile provider to use       | As in [global-settings.md](../usage/global-settings.md "mention") |
| `disableRecovery`      | `bool`                                                                            | Disable the built-in recovery system (not recommended) | `false`                                                           |

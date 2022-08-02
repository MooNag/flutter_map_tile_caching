---
description: Available on Android only
---

# 3⃣ Start In Background

{% hint style="info" %}
You should read about the [limitations and tradeoffs of background downloading](limitations.md) before you start using it.
{% endhint %}

{% hint style="danger" %}
You must comply to your tile server's ToS. Failure to do so may result in you being banned from their services.

OpenStreetMap's can be [found here](https://operations.osmfoundation.org/policies/tiles): specifically bulk downloading is discouraged, and forbidden after zoom level 13. Other servers may have different terms.

This package is not responsible for your misuse of another tile server.
{% endhint %}

```dart
FMTC.instance('storeName').download.startBackground();
```

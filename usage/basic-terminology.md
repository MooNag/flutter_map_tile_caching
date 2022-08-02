# Basic Terminology

{% hint style="info" %}
If you aren't fully familiar with flutter\_map yet, you should first read through it's detailed documentation.

{% embed url="https://docs.fleaflet.dev/" %}
flutter\_map Documentation
{% endembed %}
{% endhint %}

For development with this package, it is essential to become familiar with some terminology used throughout the documentation and API:

*   A '[Root](roots-and-stores/#root)' can hold multiple '[Stores](roots-and-stores/#store-manual-creation)'.

    There is usually only one root per application, but more complex applications may wish to use more than one. In this case, the [initialisation](initialisation.md) function can be run more than once.
* '[Browse Caching](integration.md)' (or just 'caching') is the caching performed when a user pans over a tile in a map view and it becomes visible.
* '[Bulk Downloading](../bulk-downloading/introduction.md)' is the caching performed when a user initiates a download by specifying a region to download at once.

---
description: Applies only to Stores
---

# Metadata

This library provides a very simple persistent key-value pair storage system, designed to store any custom information about the store. For example, your application may use one store per `templateUrl`, in which case, the URL can be stored in the metadata.

```dart
FlutterMapTileCaching.instance('storeName').metadata;
```

## Add

{% hint style="warning" %}
Keys are used as the name of a file. Therefore, keys must be safe, as they are not sanitized by this library.
{% endhint %}

Add a new key-value pair to the store. For example:

```dart
    add(
        key: 'key',
        value: 'value',
    );
```

## Read

Read all the key-value pairs from the store, and return them in a `Map<String, String>`. For example:

```dart
    read; // This is a getter
```

## Remove

Remove a key-value pair from the store. For example:

```dart
    remove(key: 'key');
```

## Reset

Remove all the key-value pairs from the store. For example:

```dart
    reset();
```

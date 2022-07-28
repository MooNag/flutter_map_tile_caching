# Migrator

```dart
FlutterMapTileCaching.instance.rootDirectory.migrator;
```

To migrate from older versions with different, incompatible, file structures, migration methods have been provided.

After using the snippet above, use the appropriate method(s) to reach the package version in use. These automatically check for the the structure of a previous version, and migrate it to the correct structure for one version newer. If they successfully migrated a structure, they will return `true`; otherwise (if it wasn't successful, or one wasn't found), they will return `false`.

For example, to automatically check for and migrate v4 structures to v5, use `fromV4`. It is safe to call this every time the application is loaded, and the example application demonstrates this.

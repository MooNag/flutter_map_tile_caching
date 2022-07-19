---
description: Applies to Roots and Stores
---

# Statistics

```dart
FlutterMapTileCaching.rootDirectory.stats;
FlutterMapTileCaching.instance('storeName').stats;
```

## Available APIs

| API Method/Getter                                                 | Structure | Explanation                                                                 |
| ----------------------------------------------------------------- | --------- | --------------------------------------------------------------------------- |
| [`watchChanges()`](statistics.md#watch-for-changes)``             | Both      | Use a filesystem watcher to watch for changes, useful for a `StreamBuilder` |
| [`invalidateCachedStatistics()`](statistics.md#statistic-caching) | Both      | Remove any cached statistic information                                     |
| `storesAvailable`                                                 | Roots     | List all the currently ready stores under the root                          |
| `rootSize`                                                        | Roots     | Get the current root size in KiB including all sub-stores                   |
| `rootLength`                                                      | Roots     | Get the number of tiles currently cached in all sub-stores                  |
| `storeSize`                                                       | Stores    | Get the current store size in KiB                                           |
| `storeLength`                                                     | Stores    | Get the number of tiles currently cached                                    |
| `cacheHits`                                                       | Stores    | Get the number of tiles retrieved from the store during browsing            |
| `cacheMisses`                                                     | Stores    | Get the number of tiles not retrieved from the store during browsing        |

### Watch For Changes

```dart
FMTC.instance('storeName').stats.watchChanges(
    recursive: bool,
    debounce: Duration?,
    fileSystemEvents: int,
);
```

`recursive` is only available in Roots. If `true` (default `false`), then the resulting `Stream` merges in the sub-Stores' `watchChanges` methods.

`debounce` defaults to 200ms, and is useful to remove small consecutive changes to prevent spam to your interface.

`fileSystemEvents` defaults to `FileSystemEvent.all`, and is useful to remove only some types of change from the resulting `Stream`.

Returns a `Stream<void>`, useful to trigger UI updates with other statistics.

## Statistic Caching

Many statistics are cached for better performance, as some take a long time to calculate.

If this causes problems, chain `noCache` before the below API getters/methods, like this: `stats.noCache.storeSize`.

Alternatively, clear the currently cached statistics using `invalidateCachedStatistics()`. This is automatically called when new tiles are added to the store.

# 4⃣ Listen For Progress

To listen for progress events, you can listen to the `Stream` of `DownloadProgress` events returned by the `startForeground()` method.

Listening can be done through any method, such as `listen()` or the `await for` loop.

{% hint style="warning" %}
To actually start downloading any tiles, you must attach a listener to the returned `Stream`, even if you do not plan to use the [#available-statistics](progress.md#available-statistics "mention").
{% endhint %}

## Available Statistics

| Statistic               | Type           | Explanation                                                                                                                                                                                                             |
| ----------------------- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `successfulTiles`       | `int`          | Number of tiles successfully downloaded                                                                                                                                                                                 |
| `failedTiles`           | `List<String>` | List of tile URLs that failed to download                                                                                                                                                                               |
| `maxTiles`              | `int`          | Number of expected tiles in the download region                                                                                                                                                                         |
| `successfulSize`        | `double`       | Total size of all successful tiles (in kibibytes)                                                                                                                                                                       |
| `seaTiles`              | `int`          | Number of tiles 'skipped' due to [#sea-tile-removal](../prepare.md#sea-tile-removal "mention")                                                                                                                          |
| `existingTiles`         | `int`          | Number of tiles skipped due to `preventRedownload`                                                                                                                                                                      |
| `duration`              | `Duration`     | Current duration spent downloading tiles                                                                                                                                                                                |
| `tileImage`             | `MemoryImage?` | Image of the last tile downloaded, or `null` if unavailable                                                                                                                                                             |
| `attemptedTiles`        | `int`          | Number of tiles attempted (successful + failed)                                                                                                                                                                         |
| `remainingTiles`        | `int`          | Number of tiles remaining (max - attempted)                                                                                                                                                                             |
| `seaTilesDiscount`      | `double`       | Percentage of tiles skipped due to [#sea-tile-removal](../prepare.md#sea-tile-removal "mention")                                                                                                                        |
| `existingTilesDiscount` | `double`       | Percentage of tiles skipped due to `preventRedownload`                                                                                                                                                                  |
| `percentageProgress`    | `double`       | Percentage of download currently complete                                                                                                                                                                               |
| `averageTPS`            | `double`       | <p>Average number of tiles per second being downloaded.</p><p><em>This uses a specialised exponentially smoothed moving average algorithm for better results (where more recent results affect the value more)</em></p> |
| `estTotalDuration`      | `Duration`     | Estimated duration for the entire download                                                                                                                                                                              |
| `estRemainingDuration`  | `Double`       | Estimated duration for the remaining part of the download                                                                                                                                                               |

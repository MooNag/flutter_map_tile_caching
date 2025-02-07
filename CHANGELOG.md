# Changelog

1. Major version releases change the first digit and signify major (breaking) API changes, with or without deprecation warnings
2. Minor version releases change the second digit and signify minor (breaking with deprecation warnings, or non-breaking) API changes or internal refactoring
3. Revision version releases change the third digit and signify bug fixes or documentation changes

---

## [5.1.0] - 2022/08/09

* Added import/export functionality
* Improved example application
* Improved documentation
* Fixed bugs

## [5.0.0] - 2022/08/03

* Renamed and refactored internal and public APIs, ready for release
* Added `successfulSize` statistic to `DownloadProgress`
* Improved example application
* Improved documentation
* Fixed bugs

## [5.0.0-dev.6] - 2022/07/29

* Polish and preparations for full v5 release
* Moved `migrator` into `rootDirectory` to fix bugs
* Converted `DownloadManagement` to a singleton object
* Finished example application
* Improved documentation
* Fixed bugs

## [5.0.0-dev.5] - 2022/07/25

* Improved download time estimates and added tiles per second statistic
* Added custom filesystem string sanitiser setting to `FMTCSettings`
* Improved statistic watchers
* Improved example application
* Improved documentation
* Fixed bugs

## [5.0.0-dev.4] - 2022/07/19

* Added cache hits and misses statistics
* Added v4 to v5 file structure migration methods
* Reworked `invalidateCachedStatistics`
* Improved documentation
* Fixed bugs

## [5.0.0-dev.3] - 2022/07/17

* Improved example application
* Updated Gradle for example application
* Improved documentation
* Improved background downloading implementation
* Added support for 'flutter_map' v2.0.0
* Added Windows support to example application
* Fixed multiple bugs

## [5.0.0-dev.2] - 2022/06/13

* Example application improvements
* README documentation improvements
* Deprecated `preDownloadChecksCallback`
* Added `checkTileCached` to tile provider
* Refactored and reorganised public APIs (eg. moved `tileImage` from `stats` to `manage`)

## [5.0.0-dev.1] - 2022/06/01

* Widespread syntax changes
* Added custom metadata storage functionality
* Added statistic caching to improve performance somewhat
* Start of new example application for better performance and Material 3 support
* Documentation improvements
* Specification of platform support
* Internal refactoring and reorganization

## [4.0.1] - 2022/02/28

* Fix bug #45 (on GitHub)

## [4.0.0] - 2022/02/26

* Miscellaneous changes
* Check file system watching is supported before usage
* Incorporate all pre-releases

## [4.0.0-dev.11] - 2022/02/20

* Example improvements - new example app still in progress
* Improve estimations for downloading durations (still needs tweaking)
* Upgraded Dart and Flutter versions
* Fix bug #41 (on GitHub)

## [3.0.4] - 2022/02/10

* Fix bug #41 (on GitHub)
* Bumped 'flutter_local_notifications' version to v9.2.0

## [4.0.0-dev.10] - 2022/01/26

* Fixed major performance issues
* Example improvements - new example app still in progress
* Tweaked `AsyncMapCachingManager` & `MapCachingManager`
* Replaced assertions with throws
* Internal refactoring
* Added build tools
* Recovery system reworked - needs testing
* Added linter

## [4.0.0-dev.9] - 2021/12/27

* Added new functionality: `AsyncMapCachingManager` (extension methods)
* Added new functionality: debouncing for `watch...` methods in `MapCachingManager`
* Added new functionality: `emptyStore()` in `MapCachingManager`
* Fixed inaccurate size reporting
* Example improvements - new example app still in progress
* General changes to README

## [4.0.0-dev.8] - 2021/12/09

* New example app (in progress)
* Added `coverImage()` functionality
* General improvements
* Fixed issues for web compilation (needs more testing)
* Acknowledged issue with dynamic tile source swapping (see #31 on GitHub), still needs resolving

## [4.0.0-dev.7] - 2021/11/06

* Major performance improvements through custom `ImageProvider`
* Automatic cache store creation on initialization of `StorageCachingTileProvider` and `MapCachingManager`
* Added watchable stream to `MapCachingManager` to listen to changes in statistics
* Removed 'network_to_file_image' dependency
* Fixed and improved 'browse caching' logic
* Better hidden internal constructors
* Deprecated and removed some functionality

## [4.0.0-dev.6] - 2021/10/10

* Added pre-download check functionality
* Added ability to change caching behaviour
* Rewritten tile provider part to be smaller and more efficient
* Updated & fixed example
* Project reorganisation
* Updated tests

## [4.0.0-dev.5+1] - 2021/10/08

* Deprecated circle extensions to match new 'standard'
* Pleased Flutter formatter
* Updated example
* Fixed serious `Isolate` bugs that prevented downloads by removing the isolate system
* Added 'prettyPaint'ing to `LineRegion`
* Some performance improvements and internal refactoring
* Added more Installation instructions
* *BUG* `LineRegion` does not report an estimated amount of tiles in the example
* Updated tests

## [4.0.0-dev.5] - 2021/09/27

* Added multithreading to download loop (thanks to GitHub contributor [Abdelrahman-Sherif](https://github.com/Abdelrahman-Sherif))
* Add line tile loop (not complete, some bugs)
* Added precise recovery mode (requires testing)
* Changed tests to only use one thread
* Edited README
* Taken some features out of experimental
* Removed broken `compressionQuality`
* Removed encoded polyline conversion functionality
* ... and more

## [3.0.3] - 2021/09/12

* Fix bug #32 (on GitHub)
* Update .gitignore
* Update README to recommend v4

## [4.0.0-dev.4] - 2021/09/02

* Created recovery system
* Added new examples
* Improved automated tests
* Deprecated shape chooser
* Deprecated some extension methods
* Working on example app
* Add more customization to background download notifications
* Some testing and bug fixes still required
* Update to documentation README still required

## [4.0.0-dev.3] - 2021/08/29

* Created automated tests
* Reworked `DownloadProgress()`, adding many more statistics
* Add way to rename existing store
* Large refactoring and reduction of code duplication
* Performance improvements
* Marked some experimental functionality as experimental, ready for release
* Added re-download prevention option
* Added sea tile removal
* Added compression option (needs manual testing)

## [3.0.2] - 2021/07/25

* Fix bug #20 (on GitHub)
* Updated README

## [4.0.0-dev.2] - 2021/07/20

* Bug fixes
* Re-introduction of tile count limiter
* Improve documentation

## [4.0.0-dev.1] - 2021/07/20

* Migrate to filesystem API
* Add basic preload surroundings widgets
* Fix bugs
* Improve documentation
* Allow manual control over `forceAlarmManager`, off by default
* Remove very old APIs
* Deprecate old APIs
* Removal of tile count limiter

## [3.0.1] - 2021/07/20

* Fix bug #17 (on GitHub)
* Removed an invalid example
* Updated README

## [3.0.0] - 2021/07/04

* Last quick fixes
* Publish to pub.dev
* Use AlarmManager for background tasks to resolve issues
* Deprecate old APIs

## [3.0.0-dev.2] - 2021/07/01

* Move to more appropriate date system for changelog
* Rewritten documentation
* Improved examples
* Improved easy shape chooser

## [3.0.0-dev.1] - 30/06/2021

* Huge refactoring to make methods easier to use and more flexible
* Addition of circle region
* Refactoring of square region
* Removal of tuple from main methods
* Addition of ability to exclude pure sea tiles
* Addition of multiple caching tables
* Performance improvements
* Add donation method
* Add GitHub actions
* Added easy shape chooser

## [2.0.2] - 04/06/2021

* Publish to pub.dev
* Null safety finalised

## [2.0.1] - 04/06/2021

* Attempt to publish (failed)

## [2.0.0] - 23/05/2021

* Increased default values (increased default cache limit (tiles) to 20000 and default cache duration to 31 days)
* Improved readme (added badges, simplified a calculation and increased detail on how to install and import)
* Re-organised file structure to match recommended layout
* Added changelog heading to please linter
* Fixed issues with WMS tile layer options

## [1.1.0] - 23/05/2021

* **DO NOT UPDATE TO THIS VERSION as there is a full new release coming soon**
* Enable sound null-safety (**Breaking Change:** Only SDK `>= 2.12.0` allowed)

## [1.0.1] - 09/04/2021

* Initial release
* First publish to pub.dev

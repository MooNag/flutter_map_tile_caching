# Global Settings

```dart
FlutterMapTileCaching.settings;
```

It is possible to customize package-wide defaults through this method.

## Default Tile Provider Settings (`defaultTileProviderSettings`)

Provide a set of [#tile-provider-settings](integration.md#tile-provider-settings "mention") to use when not specified by other methods, such as the tile provider getter or bulk download methods.

## Custom Filesystem String Sanitiser (`filesystemSanitiser`)

This method is commonly used to sanitise strings that will appear as the name of a directory or file in the filesystem.

The method should return a `FilesystemSanitiserResult` given a single input string. The internal situation decides whether an invalid input throws an error, or just uses the new string. For example, the tile storer just uses the valid output, whereas the store creator requires a valid input (because the output is shown to the user, so must be the same as the input).

The default method is suitable for most use-cases, but you may wish to override this for added reliability.

### Filesystem Sanitiser Result (`FilesystemSanitiserResult)`

The object returned from any valid filesystem string sanitiser. Has a `validOutput` string, which is the sanitised result, and an `errorMessages` list of strings, which can be empty if the input string was valid or contain one or more errors.

### Form Field Validator (`filesystemFormFieldValidator`)

This method is available from the root of the settings, and uses the `filesystemSanitiser` to validate (throw error if invalid) the input string.

Is suitable for direct usage (no wrapper function needed) in the `validator` property of the `TextFormField`.

# @react-native/community-cli-plugin

> This is an internal dependency of React Native. **Please don't depend on it directly.**

CLI entry points supporting core React Native development features.

Formerly [@react-native-community/cli-plugin-metro](https://www.npmjs.com/package/@react-native-community/cli-plugin-metro).

## Commands

### `start`

Start the React Native development server.

#### Usage

```sh
react-native start [options]
```

#### Options

| Option | Description |
| - | - |
| `--port <number>` | Set the server port. |
| `--host <string>` | Set the server host. |
| `--projectRoot <path>` | Set the path to the project root. |
| `--watchFolders <list>` | Specify additional folders to be added to the watch list. |
| `--assetPlugins <list>` | Specify additional asset plugins. |
| `--sourceExts <list>` | Specify additional source extensions to bundle. |
| `--max-workers <number>` | Set the maximum number of workers the worker-pool will spawn for transforming files. Defaults to the number of the cores available on your machine. |
| `--transformer <string>` | Specify a custom transformer. |
| `--reset-cache` | Remove cached files. |
| `--custom-log-reporter-path <string>` | Specify a module path exporting a replacement for `TerminalReporter`. |
| `--https` | Enable HTTPS connections. |
| `--key <path>`| Specify path to a custom SSL key. |
| `--cert <path>` | Specify path to a custom SSL cert. |
| `--config <string>` | Path to the CLI configuration file. |
| `--no-interactive` | Disable interactive mode. |

### `bundle`

Build the bundle for the provided JavaScript entry file.

#### Usage

```sh
react-native bundle --entry-file <path> [options]
```

#### Options

| Option | Description |
| - | - |
| `--entry-file <path>` | Set the path to the root JavaScript entry file. |
| `--platform <string>` | Set the target platform (either `"android"` or `"ios"`). Defaults to `"ios"`. |
| `--transformer <string>` | Specify a custom transformer. |
| `--dev [boolean]` | If `false`, warnings are disabled and the bundle is minified. Defaults to `true`. |
| `--minify [boolean]` | Allows overriding whether bundle is minified. Defaults to `false` if `--dev` is set. Disabling minification can be useful for speeding up production builds for testing purposes. |
| `--bundle-output <string>` | Specify the path to store the resulting bundle. |
| `--bundle-encoding <string>` | Specify the encoding for writing the bundle (<https://nodejs.org/api/buffer.html#buffer_buffer>). |
| `--sourcemap-output <string>` | Specify the path to store the source map file for the resulting bundle. |
| `--sourcemap-sources-root <string>` | Set the root path for source map entries. |
| `--sourcemap-use-absolute-path` | Report `SourceMapURL` using its full path. |
| `--max-workers <number>` | Set the maximum number of workers the worker-pool will spawn for transforming files. Defaults to the number of the cores available on your machine. |
| `--assets-dest <string>` | Specify the directory path for storing assets referenced in the bundle. |
| `--reset-cache` | Remove cached files. |
| `--read-global-cache` | Attempt to fetch transformed JS code from the global cache, if configured. Defaults to `false`. |
| `--config <string>` | Path to the CLI configuration file. |

### `ram-bundle`

Build the [RAM bundle](https://reactnative.dev/docs/ram-bundles-inline-requires) for the provided JavaScript entry file.

#### Usage

```sh
react-native ram-bundle --entry-file <path> [options]
```

#### Options

Accepts all options supported by [`bundle`](#bundle) and the following:

| Option | Description |
| - | - |
| `--indexed-ram-bundle` | Force the "Indexed RAM" bundle file format, even when building for Android. |

# Contributing to WebView Native UI

Thanks for your interest in improving WebView Native UI.

## Where to contribute

Please open issues and pull requests in the repository that owns the affected functionality:

| Area                                                                                                                               | Repository                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Native/Web coordination infrastructure: placement, scrolling and overlays                                                          | [Engine](https://github.com/webview-native-ui/engine)                       |
| Shared control projection/rendering in `packages/native-ui-core`, or Capacitor registration, bridge calls, events and installation | [Capacitor Plugin](https://github.com/webview-native-ui/capacitor-plugin)   |
| Cordova bridge, lifecycle, installation, generated-copy build or packaged theme integration                                        | [Cordova Plugin](https://github.com/webview-native-ui/cordova-plugin)       |
| iOS theme styles, Web layout, Ionic transitions, or the combined demo                                                              | [Ionic iOS Theme](https://github.com/webview-native-ui/ionic-theme-ios27)   |
| Material Design 3 theme behavior                                                                                                   | [Ionic MD3 Theme](https://github.com/webview-native-ui/ionic-theme-md3)     |
| Shared theme utilities or build tools                                                                                              | [Ionic Theme Utils](https://github.com/webview-native-ui/ionic-theme-utils) |
| Organization profile or shared community files                                                                                     | [.github](https://github.com/webview-native-ui/.github)                     |

If ownership is unclear, report the issue where you encountered it and include a reproduction and all relevant package versions. Maintainers can route it; there is no need to open duplicate issues across repositories.

## Before reporting a bug

- Search existing issues and documentation.
- Provide affected package versions, platform and OS versions, and relevant Capacitor, Cordova or Ionic versions. For combined apps, include the Engine, plugin, and theme versions. When using Cordova's bundled theme, include the Core revision and theme version from the installed package's `shared/ORIGIN.json`; for native dependency problems, include the resolved SwiftPM, CocoaPods, or Maven versions.
- Include reproduction steps, expected behavior and actual behavior.
- Remove credentials, personal information and API keys from logs.
- Include a screenshot or short video when investigating rendering behavior.

## Pull requests

- Discuss significant API or architectural changes in an issue before implementing them.
- Keep changes focused, with tests or reproducible examples where practical.
- Update documentation for user-visible changes.
- Describe platform-specific limitations and compatibility considerations.
- Follow the target repository's development and testing instructions.

## Project boundaries

Keep native/Web coordination infrastructure in Engine, shared control projection/rendering in the Capacitor repository's private `packages/native-ui-core` workspace, runtime-specific bridge code in its adapter, and Web styling/layout in the themes. Core is embedded in plugin distributions and does not require a separate package release. Keep host SDK dependencies out of Core and Engine's shared implementation, keep Ionic integrations optional where documented, and preserve existing application-facing APIs.

Cordova consumes generated copies of Core at the commit pinned in `core-source.json`. Fix shared behavior in the Capacitor repository first, then update the Cordova pin and rebuild. Fix theme behavior in the theme repository; Cordova copies the pinned published theme at build time and redirects integration imports to its Core. Do not patch generated files in Cordova's `shared/`, `dist/` or `www/`, or the generated Android Core copy in the Capacitor repository. Follow each repository's generation and validation commands.

Keep Cordova-specific fixes in its adapter. The smaller Cordova support scope does not require duplicating the shared implementation's full test suite or creating an independent Core release process.

For changes spanning repositories, describe the dependency and release order. Distinguish validation against local candidate packages from validation against published versions. Common implementation tests belong with that implementation; adapter tests and demo integration tests belong with their respective consumers. Keep temporary verification scripts, generated test projects, and local dependency paths out of pull requests.

## Security

Do not disclose vulnerabilities in public issues. See [SECURITY.md](SECURITY.md).

Please follow the [Code of Conduct](CODE_OF_CONDUCT.md). Contributions are governed by the target repository's own license.

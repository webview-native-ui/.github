# Contributing to WebView Native UI

Thanks for your interest in improving WebView Native UI.

## Where to contribute

Please open issues and pull requests in the repository that owns the affected functionality:

| Area                                                                         | Repository                                                                  |
| ---------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| Shared native/Web coordination, projection, or shared control implementation | [Engine](https://github.com/webview-native-ui/engine)                       |
| Capacitor registration, bridge calls, events, or plugin installation         | [Capacitor Plugin](https://github.com/webview-native-ui/capacitor-plugin)   |
| iOS theme styles, Web layout, Ionic transitions, or the combined demo        | [Ionic iOS Theme](https://github.com/webview-native-ui/ionic-theme-ios27)   |
| Material Design 3 theme behavior                                             | [Ionic MD3 Theme](https://github.com/webview-native-ui/ionic-theme-md3)     |
| Shared theme utilities or build tools                                        | [Ionic Theme Utils](https://github.com/webview-native-ui/ionic-theme-utils) |
| Organization profile or shared community files                               | [.github](https://github.com/webview-native-ui/.github)                     |

If ownership is unclear, report the issue where you encountered it and include a reproduction and all relevant package versions. Maintainers can route it; there is no need to open duplicate issues across repositories.

## Before reporting a bug

- Search existing issues and documentation.
- Provide affected package versions, platform and OS versions, and relevant Capacitor, Cordova or Ionic versions. For combined apps, include the Engine, plugin, and theme versions; for native dependency problems, include the resolved SwiftPM, CocoaPods, or Maven versions.
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

Keep shared native/Web behavior in Engine, runtime-specific bridge code in its plugin, and Web styling/layout in the themes. Engine supports embedding in both Capacitor and Cordova plugins; do not introduce a required Capacitor dependency into its shared control implementation. Keep Ionic integrations optional where documented and preserve existing application-facing APIs.

For changes spanning repositories, describe the dependency and release order. Distinguish validation against local candidate packages from validation against published versions. Common implementation tests belong with that implementation; adapter tests and demo integration tests belong with their respective consumers. Keep temporary verification scripts, generated test projects, and local dependency paths out of pull requests.

## Security

Do not disclose vulnerabilities in public issues. See [SECURITY.md](SECURITY.md).

Please follow the [Code of Conduct](CODE_OF_CONDUCT.md). Contributions are governed by the target repository's own license.

# Beyond the WebView.

**Bring Web and Native UI into one experience.**

WebView Native UI is an independent open-source initiative for bringing native interfaces and Web content together in WebView-based applications.

## Projects

| Project                                                                               | Package                       | Purpose                                                                                                                              |
| ------------------------------------------------------------------------------------- | ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| [Engine](https://github.com/webview-native-ui/engine)                                 | `@webview-native-ui/engine`   | Native/Web coordination for Capacitor and Cordova plugin authors: placement, scrolling, overlays, and shared control infrastructure. |
| [Capacitor Plugin](https://github.com/webview-native-ui/capacitor-plugin)             | `@rdlabo/capacitor-native-ui` | Add native controls to Capacitor apps, with standard HTML and optional Ionic integration.                                            |
| [Ionic iOS Theme](https://github.com/webview-native-ui/ionic-theme-ios27)             | `@rdlabo/ionic-theme-ios27`   | iOS styling, motion, and Web layout for Ionic apps; also hosts the combined theme and Native UI demo.                                |
| [Ionic Material Design 3 Theme](https://github.com/webview-native-ui/ionic-theme-md3) | `@rdlabo/ionic-theme-md3`     | Material Design 3 styling for Ionic apps.                                                                                            |
| [Ionic Theme Utils](https://github.com/webview-native-ui/ionic-theme-utils)           | `@rdlabo/ionic-theme-utils`   | Shared theme utilities, animation helpers, Sass mixins, and theme build tools.                                                       |

## Choose a starting point

- **Add native controls to a Capacitor app:** start with the [Capacitor plugin setup guide](https://github.com/webview-native-ui/capacitor-plugin/blob/main/docs/setup.md).
- **Build a Capacitor or Cordova plugin:** start with the [Engine guides](https://github.com/webview-native-ui/engine/tree/main/docs/getting-started).
- **Style an Ionic app:** start with the [iOS theme](https://github.com/webview-native-ui/ionic-theme-ios27) or [MD3 theme](https://github.com/webview-native-ui/ionic-theme-md3).

Engine provides the shared foundation; runtime-specific plugins expose it to applications, and themes own Web styling and layout. Installing a theme does not activate native controls. Cordova support currently means integrating Engine into a Cordova plugin; an application-facing Cordova Native UI plugin is not yet available.

The projects release independently. Follow each package's compatibility and setup guide. Documentation on `main` can include changes that are not yet published; use the documentation for your installed release when available.

## See it in action

Native controls can scroll with Web content, while Web overlays can appear above native controls, without abandoning Web layouts and navigation.

[Watch the Engine demo](https://github.com/user-attachments/assets/2768f014-7325-49c7-b848-25052756c36d) · [Documentation](https://github.com/webview-native-ui/engine/tree/main/docs) · [How it works](https://github.com/webview-native-ui/engine/blob/main/docs/concepts.md)

## Building on existing ecosystems

We complement existing WebView frameworks rather than replacing them. The Engine supports Capacitor and Cordova plugin development; the Ionic themes are separate tools with their own support scopes.

## Contributing

Issues, examples, documentation improvements, and pull requests are welcome. Please start in the relevant repository and read the [contribution guide](https://github.com/webview-native-ui/.github/blob/main/CONTRIBUTING.md).

WebView Native UI is not an official Ionic, Capacitor, or Cordova project.

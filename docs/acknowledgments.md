## Third-party notices

The source tree vendors the following dependencies. Their pinned license texts are included with the
vendored copies so this repository does not rely on mutable external links for required notices.

- **ShortcutRecorder** — `lwouis/ShortcutRecorder` commit
  [`52c6273`](https://github.com/lwouis/ShortcutRecorder/commit/52c6273d233f7794e4fd5d22f50d2de0e4e41b19),
  licensed under CC BY 4.0. [License text](../vendor/ShortcutRecorder/LICENSE.txt). The vendoring process
  patches bundle-resource lookup for Swift Package Manager; see `vendor/scripts/update_shortcut_recorder.sh`.
  AltTabLocal adds no further changes to the vendored copy.
- **Sparkle** — version [2.9.1](https://github.com/sparkle-project/Sparkle/tree/2.9.1), licensed under
  MIT plus the bundled external notices reproduced in its license. [License text](../vendor/Sparkle/LICENSE).
  AltTabLocal disables updater construction and startup but retains the upstream vendored source and helpers.
- **Visual Studio App Center SDK for Apple platforms** — version
  [4.3.0](https://github.com/microsoft/appcenter-sdk-apple/tree/4.3.0), licensed under MIT.
  [License text](../vendor/AppCenter/LICENSE). AltTabLocal disables App Center crash-reporting startup but
  retains the upstream vendored source.
- **PLCrashReporter** — version
  [1.11.1](https://github.com/microsoft/plcrashreporter/tree/1.11.1), distributed as part of the vendored
  App Center package and licensed under MIT with an Apache-2.0-covered portion.
  [License text](../vendor/AppCenter/PLCrashReporter-LICENSE).

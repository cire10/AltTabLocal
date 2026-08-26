# AltTabLocal

AltTabLocal is an unofficial, source-only fork of
[AltTab v11.5.0](https://github.com/lwouis/alt-tab-macos/releases/tag/v11.5.0). It starts from
upstream commit [`941d841`](https://github.com/lwouis/alt-tab-macos/commit/941d841e7bacb6dec2134e11df93e6991b6584fc)
and keeps the upstream GPL-3.0 license.

This fork is designed to coexist with the official app:

- App name: `AltTabLocal`
- Bundle ID: `com.erictang.AltTabLocal`
- Automatic updates, telemetry startup, and crash-reporting startup are disabled
- Features that upstream gates behind Pro operate locally without a trial, account, keychain record,
  purchase, or licensing-network request
- Fresh installs default to a 0 ms display delay and Small thumbnails, matching the responsive settings
  used for the tested local installation

See [LOCAL_CHANGES.md](LOCAL_CHANGES.md) for the complete change summary. This project is not affiliated
with or supported by the upstream AltTab project.

The official app and AltTabLocal can be installed side by side, but do not run both at the same time:
their global shortcuts and window-monitoring hooks can conflict.

## Build locally

Requirements: macOS and full Xcode 26. The current source was tested with Xcode 26.6.

```sh
git clone https://github.com/cire10/AltTabLocal.git
cd AltTabLocal
xcodebuild \
  -project alt-tab-macos.xcodeproj \
  -scheme Release \
  -configuration Release \
  -derivedDataPath DerivedData \
  build
```

The locally signed app will be at:

```text
DerivedData/Build/Products/Release/AltTabLocal.app
```

Open that folder and drag `AltTabLocal.app` into `/Applications`. macOS will ask for Accessibility
and Screen Recording permissions on first use. Because the build is ad-hoc signed and not notarized,
only run an app that you built yourself from source you reviewed.

## Verify

```sh
xcodebuild test \
  -project alt-tab-macos.xcodeproj \
  -scheme Test \
  -configuration Release \
  -destination 'platform=macOS,arch=arm64' \
  -derivedDataPath DerivedDataTests
```

## License and upstream

- License: [GPL-3.0](LICENCE.md)
- Third-party notices: [docs/acknowledgments.md](docs/acknowledgments.md)
- Official project: [lwouis/alt-tab-macos](https://github.com/lwouis/alt-tab-macos)

The repository's GitHub funding links intentionally continue to support the upstream AltTab maintainer.

# AltTabLocal

This public source fork is based on the official AltTab v11.5.0 source at commit
`941d841e7bacb6dec2134e11df93e6991b6584fc`.

Local changes made on 2026-08-24 and 2026-08-25:

- Uses the distinct app name `AltTabLocal` and bundle ID `com.erictang.AltTabLocal` while retaining
  the upstream `11.5.0` version number.
- Makes the repository's Pro-gated features available locally without a license, trial, keychain
  record, or licensing-network request.
- Removes purchase, account, upgrade, update, feedback, support, and crash-reporting UI entry points.
- Removes Pro badges from settings controls and defaults local start-at-login to off so it cannot
  automatically race an installed official AltTab copy.
- Defaults fresh installations to a 0 ms display delay and Small thumbnails, matching the responsive
  settings selected after testing the local build.
- Does not construct or start Sparkle or AppCenter, and points dormant service URLs at the reserved
  `.invalid` top-level domain.
- Defaults updates to manual and crash reporting to never.
- Uses an ad-hoc local signature and is not notarized. This repository distributes source; users
  should build the app locally rather than redistribute an unsigned binary.

The upstream GPL-3.0 license remains in `LICENCE.md`. This fork is unofficial and is not supported by
the upstream AltTab project. Pinned licenses for vendored dependencies are included alongside their
source under `vendor/` and indexed in `docs/acknowledgments.md`.

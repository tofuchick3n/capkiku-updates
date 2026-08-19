<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
capkiku 1.0.9 makes Screen Recording permission recovery clear and reliable after an update.

### Fixed

- Screen Recording can now be requested again when macOS keeps a stale or denied permission after an update.
- If macOS does not show capkiku or a permission prompt, the app opens the correct Settings pane and explains how to add `capkiku.app` with **+**.
- When macOS accepts Screen Recording but requires a full relaunch, capkiku now says **Restart required** and offers **Quit capkiku** instead of showing contradictory recovery instructions.
- Development packages use a separate app identity with no production update feed, preventing test builds from interfering with the production app's privacy permissions.
- Release verification now blocks updates that change capkiku's designated code requirement and would invalidate existing macOS permissions.

### Verify the download

SHA-256 (`capkiku.zip`): `fbbd3bcc2eb53d041db403fff9ff5404c16cb6507074ec9be3b030b8035a66bc`

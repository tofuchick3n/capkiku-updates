<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
capkiku 1.0.8 adds purposeful motion and completes the app-wide visual polish pass.

### Changed

- Review, OCR, and save states now use brief, purposeful motion that follows macOS Reduce Motion. The Review inspector uses the native trailing-column transition, and Settings carries its selection between panes.
- Action buttons now use one content-sized macOS treatment: teal capsules for primary actions and matching neutral capsules for secondary actions.
- Preview and Saved Capture keep their content clean instead of decorating it with capture brackets.
- Review Audio no longer repeats the window title inside the content.
- Copy actions in Review, Receipts, and Recents now confirm only after the text reaches the clipboard.

### Fixed

- Launch-time recovery windows now come to the foreground instead of opening behind another app.
- Review keeps its three panes within the window while the inspector opens and closes.
- Settings booleans use one compact macOS switch, permission actions share one height, dark permission states stay legible, and Review toolbar hover feedback no longer draws doubled button chrome.
- The region selector keeps Kiku and the **FRAME!** prompt farther below the menu bar without overlapping each other.
- The final setup step no longer frames Kiku with decorative capture corners.

### Verify the download

SHA-256 (`capkiku.zip`): `5cdc3747a2cf5eb292af54720cfe682b6f9282213bb6344690d296c047900045`

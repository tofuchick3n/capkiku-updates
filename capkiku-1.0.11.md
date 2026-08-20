<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
capkiku 1.0.11

### Fixed

- System Audio status now reports only what capkiku can verify from a real recording. Ambiguous tap failures no longer claim macOS denied permission, and the app explains how to retry or check System Settings.
- First-use on-device transcription now discloses Apple’s macOS 26 speech-model download, keeps the download and failure status visible, and clearly shows transcription problems in Review Audio and the saved receipt without implying audio was uploaded.
- Region capture now waits briefly for ScreenCaptureKit and macOS to agree on the complete display layout. It never opens an incomplete set of overlays, and gives a clear retry message if displays are still changing.
- Recent captures now refresh stale security bookmarks when opened, revealed, copied, or moved to Trash, while fast read-only availability checks keep Finder moves and macOS bookmark updates from making the window sluggish.
- Stopping an audio recording now drains callbacks that are already writing before finalizing the files, preventing rapid start/stop timing from dropping a tail buffer or racing writer teardown.

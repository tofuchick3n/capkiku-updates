<!-- sparkle-sign-warning:
IMPORTANT: This file was signed by Sparkle. Any modifications to this file requires updating signatures in appcasts that reference this file! This will involve re-running generate_appcast or sign_update.
-->
capkiku 1.0.12

### Added

- Scrolling capture: outline a region, keep the pointer inside, and capkiku scrolls and stitches the page. A floating panel can pause, resume, or finish, and a teal outline marks the selected area.

### Changed

- Review’s Copy Text control is a single outlined capsule, not a gray pill sitting on the toolbar glass.
- Scrolling capture’s introduction and Accessibility prompts are compact Kiku cards instead of long system alerts.
- Review’s inspector slides in and out from the trailing edge instead of snapping closed.

### Fixed

- Scrolling capture now ignores on-screen chrome that stays put, so pages with sticky sidebars and headers (for example X Articles) stitch instead of pausing with “Content didn’t line up.” A spinner or other local animation cannot append a strip, a tall article column in a wide crop still stitches, a moving sidebar widget cannot poison the article column, and a sparse sticky page pauses instead of being cut short.
- If a scrolling frame still cannot line up, capture keeps scrolling until the page stops moving instead of pausing mid-article. It still stops at the end of the content, the 90-second limit, or Done.
- Scrolling capture no longer keeps a clipped OCR reading next to the clean one of the same line.
- Control Scrolling and Screen Recording no longer open System Settings on top of the macOS prompt, including after a TCC reset that still leaves an old “Request Again” state. After you allow Control Scrolling, capkiku comes back to the front.
- After macOS accepts Screen Recording, capkiku relaunches **this same app** instead of quitting and leaving you to reopen it from Applications. That keeps the Dev package from being replaced by the production app in `/Applications`. The relaunch also runs when you return from the system prompt: `CGRequestScreenCaptureAccess` often returns before Allow, and this process still cannot see the grant.
- Scrolling capture now asks for Control Scrolling before the region overlay, so granting it cannot leave the menu stuck on “Recognizing text” with Capture grayed out. The menu says “Waiting for Control Scrolling,” and Cancel Capture ends that wait without quitting.
- Capture Scrolling Region relaunches this same app **once** when Accessibility is on but this process still cannot scroll, then continues the capture. It does not reopen Settings or restart in a loop.
- Cancel Capture during the Control Scrolling wait now ends that wait. Allowing Accessibility afterward no longer relaunches capkiku or resumes the canceled capture.

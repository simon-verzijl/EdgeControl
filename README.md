# EdgeControl

EdgeControl turns the edges of your Mac trackpad into controls for brightness, volume, and media playback.

## What it can do

- Swipe along a selected edge to adjust display brightness or audio volume. Choose any trackpad edge; the sides use up/down swipes, while the top and bottom use left/right swipes.
- Enable EDR Headroom on supported displays to raise SDR brightness above 100%, up to the display's supported limit (capped at 200%). The settings overview shows the current EDR brightness.
- Tap a selected corner to mute or unmute audio, or to toggle media playback. EdgeControl shows a HUD when either action is triggered.
- Swipe an unassigned top or bottom edge to skip to the previous or next track.
- Adjust edge width and sensitivity, enable fine control, require Fn or Control, freeze the pointer during gestures, and turn haptic feedback on or off.
- Show or hide the menu bar item and launch EdgeControl at login.

## Install the release

The downloadable app is ad-hoc signed for this project, but it is not signed with an Apple Developer ID or notarized. macOS may therefore report that `EdgeControl.app` is damaged after downloading it in a browser.

After unzipping the release into `~/Downloads`, remove the quarantine attribute and open the app:

```sh
xattr -dr com.apple.quarantine ~/Downloads/EdgeControl.app
open ~/Downloads/EdgeControl.app
```

Only run this command for a release you downloaded from the official EdgeControl repository and trust. It removes macOS's downloaded-file quarantine flag for this app; it does not modify the app's code.

## Build and run

Open `EdgeControl.xcodeproj` in Xcode and press **Run**. To build from Terminal:

```sh
xcodebuild -project EdgeControl.xcodeproj -scheme EdgeControl -destination 'platform=macOS' CODE_SIGNING_ALLOWED=NO build
```

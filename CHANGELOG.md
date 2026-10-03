## Anilove 6.1.22

This release improves automatic intro and outro skipping by ensuring the app has the episode runtime before it requests skip markers.

### Improvements

- **More reliable auto-skip data:** The app now waits for the video player to report the episode duration before querying AniSkip. AniSkip uses runtime when finding skip markers; requesting too early with a duration of `0` could return no results.
- **Intro and outro skipping:** When skip markers are available and auto-skip is enabled, playback can skip the marked opening or ending segment.
- **Provider skip markers:** Provider-supplied intro and outro markers continue to be supported alongside AniSkip data.
- **Playback setting:** The existing **Auto-skip intro and outro** option remains available under **Settings → Playback**.

### Availability

Auto-skip depends on skip data being available for the anime and episode. If neither AniSkip nor the provider supplies markers, there may be no segment to skip.

### Backend note

The proxy CDN allowlist fixed

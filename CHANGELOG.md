# Changelog

All notable changes to Dilo are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.17.1] - 2026-10-22

### Fixed

- After installing an update, Dilo could reopen the old copy it was running from (for
  example, the portable version) instead of the newly installed one, so it kept offering
  the same update. It now always reopens the installed copy.

## [1.17.0] - 2026-10-22

### Added

- A four-step introduction the first time Dilo opens, available again from Settings.
- A Settings window with sections for translation, other apps, appearance, general options
  and version information.
- Light theme and a "Match Windows" option that follow changes instantly, without restarting.
- Translation history: the last 50 translations from the main window, encrypted on your PC.
- Listen buttons that read the text or the translation aloud with the voices in Windows.
- Clear button for the text box, and text size control with <kbd>Ctrl</kbd> + mouse wheel.
- System tray icon. Dilo can stay in the tray when the window is closed and start with Windows.
- When you close the window, Dilo asks whether to keep running in the tray or quit, with an
  option to remember your choice.
- An error notice with a **Retry** button when a translation fails.
- A notice when Dilo detects the language you are typing in and switches direction.
- Animations throughout: a loading screen, the window entrance, the road line moving while
  Dilo translates, flipping language signs, paint flecks when you copy and an animated
  close prompt. They are turned off when Windows animation effects are off.

### Changed

- The main window is simpler: everything except translating moved to Settings, and status
  messages use plain language.
- The floating translation card stays open while the pointer is over it and remains visible
  longer for longer text.
- "Copied" is confirmed on the Copy button itself.
- The window remembers its size and position.
- Opening Dilo while it is already running brings the existing window forward instead of
  starting a second copy.

### Security

- Password fields and password managers are never read while "Translate where you type" is on.
- The AI API key is stored encrypted with Windows Data Protection (DPAPI). Keys saved in plain
  text by earlier versions are encrypted automatically.
- Diagnostic logs are capped at about 1 MB.

## [1.16.0] - 2026-10-21

### Added

- In-app updates: Dilo checks GitHub Releases on startup and on demand, verifies the
  installer's SHA-256 checksum, installs the update and reopens itself.
- The translation card can be dragged anywhere and remembers its position.
- "Open Dilo" option at the end of the installer.
- Status indicator showing whether Dilo is ready, translating or has hit an error.
- Clear Windows version check in the installer.

### Changed

- New visual identity: road-sign typography, a two-lane layout for the two languages and a
  new app icon.
- "Paste where I typed" is now "Replace what I wrote" and replaces only the sentence you
  wrote, never the rest of the field.
- When Google Translate is unavailable, AI translation is used before MyMemory if an API
  key is set.

### Fixed

- Google Translate requests were rejected with HTTP 429, so every translation fell back
  to MyMemory.
- MyMemory could return unrelated user-submitted translations; its machine translation is
  now used.
- Replacing text in other apps did nothing on 64-bit Windows, and in Discord the
  translation was added after the original sentence instead of replacing it.
- Typing accented letters (á, é, ñ) in other apps broke while "Translate where you type"
  was on.
- "Translate where you type" could stop working after a while.
- Copying while another app held the clipboard closed Dilo.
- The translation card could stay on "Translating…" when the same sentence was repeated.
- <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>T</kbd> could open developer tools in Chrome and Edge.
- Translated `.docx` files duplicated text boxes and lost spaces between words.

## [1.15.0] - 2026-10-18

### Added

- First release: live English ⇄ Spanish translation with automatic language detection,
  casual AI mode, translation in other apps, selection shortcut and document translation.

[Unreleased]: https://github.com/Grawkles/Dilo-releases/compare/v1.17.1...HEAD
[1.17.1]: https://github.com/Grawkles/Dilo-releases/releases/tag/v1.17.1
[1.17.0]: https://github.com/Grawkles/Dilo-releases/releases/tag/v1.17.0
[1.16.0]: https://github.com/Grawkles/Dilo-releases/releases/tag/v1.16.0
[1.15.0]: https://github.com/Grawkles/Dilo-releases/blob/main/CHANGELOG.md#1150---2026-10-18

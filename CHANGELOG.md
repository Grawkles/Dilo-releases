# Changelog

All notable changes to Dilo are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

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

[Unreleased]: https://github.com/Grawkles/Dilo-releases/compare/v1.16.0...HEAD
[1.16.0]: https://github.com/Grawkles/Dilo-releases/releases/tag/v1.16.0
[1.15.0]: https://github.com/Grawkles/Dilo-releases/blob/main/CHANGELOG.md#1150---2026-10-18

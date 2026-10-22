# Security policy

## Supported versions

Only the latest release receives fixes. Update from within Dilo or download the
[latest installer](https://github.com/Grawkles/Dilo-releases/releases/latest).

| Version | Supported |
|---|---|
| 1.17.x | Yes |
| < 1.17 | No |

## How updates are protected

- Dilo only downloads installers attached to releases of this repository
  (`github.com/Grawkles/Dilo-releases`), always over HTTPS.
- Before installing, Dilo compares the installer's SHA-256 checksum with the one GitHub
  publishes for that file. If they differ, the update is discarded.
- Installers are not code-signed yet. You can verify any download manually as described in
  the [README](README.md#verifying-your-download).

## How your data is protected

- Your AI API key and your translation history are encrypted with Windows Data Protection
  (DPAPI), so only your Windows account on this PC can read them.
- "Translate where you type" ignores password fields and password managers entirely.

## Reporting a vulnerability

Please do not report security problems in public issues. Use
[private vulnerability reporting](https://github.com/Grawkles/Dilo-releases/security/advisories/new)
and include the affected version, the steps to reproduce and the impact you observed.
You will receive a response as soon as possible.

# Hostwing downloads

Installer host for the Microsoft Store submission of **Hostwing** — a multi-protocol
remote-desktop console for Windows. Source lives in a private repository.

The Microsoft Store requires the package URL to return the file directly, with no HTTP
redirect. GitHub Releases answers with a 302 to a signed, short-lived CDN URL, which
Partner Center rejects, so the MSI is served from this repository instead.

## Files

| File | Size | SHA-256 |
|---|---|---|
| `Hostwing-1.8.0-x64.msi` | 69,025,792 bytes | `858042C7D9C2A83DA27F02E1CE75833321AD8F39E3ED714CAB9A7E436B5A4ABB` |

## Notes

- One file per released version. Existing files are never modified or deleted, because
  the Store re-downloads the package it certified and fails on a byte mismatch.
- The MSI installs per-user to `%LOCALAPPDATA%\Programs\Hostwing` and needs no
  administrator rights.
- Privacy policy: https://fsahaf.github.io/Hostwing/PRIVACY.html
- Licence terms: https://fsahaf.github.io/Hostwing/EULA.html

# Hostwing downloads

Installer host for the Microsoft Store submission of **Hostwing** - a multi-protocol
remote-desktop console for Windows. Source lives in a private repository.

The Microsoft Store requires the package URL to return the file directly, with no HTTP
redirect. GitHub Releases answers with a 302 to a signed, short-lived CDN URL, which
Partner Center rejects, so the MSI is served from this repository instead.

## Files

| File | Size | SHA-256 |
|---|---|---|
| `releases/1.8.1-peruser/Hostwing-1.8.1-user-x64.msi` | 69,013,504 bytes | `1D37A742F6EB84D21ED4B20FF16787C2C41C3893E5B710178868B57205EB926C` |
| `releases/1.8.1/Hostwing-1.8.1-x64.msi` | 69,013,504 bytes | `E87CC591CA826D6124B6A10C8AA85CBAF295FA9EFA623927D6970FECEC1BE61C` |
| `releases/1.8.0/Hostwing-1.8.0-x64.msi` | 69,025,792 bytes | `2C1C78FB73CB09BC9E9824A5EDB5E6EEB35BEF344783CF7AD61020D916A181F6` |

## Direct URLs

```
https://raw.githubusercontent.com/fsahaf/Hostwing-downloads/main/releases/1.8.1-peruser/Hostwing-1.8.1-user-x64.msi
https://raw.githubusercontent.com/fsahaf/Hostwing-downloads/main/releases/1.8.1/Hostwing-1.8.1-x64.msi
https://raw.githubusercontent.com/fsahaf/Hostwing-downloads/main/releases/1.8.0/Hostwing-1.8.0-x64.msi
```

## Install scope

`1.8.1` is per-machine: `C:\Program Files\Hostwing`, an all-users Start menu entry, an
HKLM uninstall entry, and one administrator prompt during installation.

`1.8.1-peruser` is per-user: `%LOCALAPPDATA%\Programs\Hostwing`, a Start menu entry and
uninstall entry for the installing user only, and **no elevation at all**, so a standard
user can install it. It is a diagnostic build for the Store certification requirement
that the package install when logged in as a standard user.

## Notes

- One directory per released version. Existing files are never modified or deleted, because
  the Store re-downloads the package it certified and fails on a byte mismatch. A new build
  gets a new directory, which also gives Partner Center a URL it has not cached a
  validation verdict for.
- Both 1.8.1 packages install `Hostwing` by `Farooq Sahaf` and never touch `%APPDATA%\Hostwing`.
- Privacy policy: https://fsahaf.github.io/Hostwing/PRIVACY.html
- Licence terms: https://fsahaf.github.io/Hostwing/EULA.html

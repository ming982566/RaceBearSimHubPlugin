# Release Notes

## 0.1.1

- Adds current and latest plugin version information to the settings footer.
- Checks the fixed public GitHub repository for newer stable Releases.
- Downloads only the expected Win32 package and checksum assets.
- Verifies HTTPS hosts, SHA-256, archive paths, and assembly versions.
- Applies updates after SimHub exits through an independent updater.
- Backs up both plugin and SDK DLLs and rolls back failed replacement.

This is the first public online-update release. The installed `0.1.0`
baseline is retained for the end-to-end update test.

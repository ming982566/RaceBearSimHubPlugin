# RaceBear SimHub Plugin

This repository hosts public binary releases for the RaceBear SimHub CAN
plugin. The plugin source code is maintained privately and is not published in
this repository.

## Installation

Download the latest `RaceBearSimHubPlugin-X.Y.Z-win32.zip` from GitHub
Releases. Exit SimHub before the initial manual installation, then copy
`RaceBearSimHubPlugin.dll` and `RaceBearSDK.dll` into the SimHub installation
directory.

After the initial installation, the plugin can check this repository for a
newer Release. A verified update is applied by the included updater only after
SimHub exits and both installed DLLs are unlocked.

## Release Assets

- `RaceBearSimHubPlugin-X.Y.Z-win32.zip`: plugin, matching x86 SDK, updater,
  and version metadata.
- `RaceBearSimHubPlugin-X.Y.Z-win32.zip.sha256`: SHA-256 checksum.
- `update-manifest.json`: public release metadata.

The updater does not force-terminate SimHub. Keep the motion platform and CAN
devices in a safe state before starting an update.

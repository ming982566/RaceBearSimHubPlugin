# Release Notes

## 0.1.17

- Adds motor parameter synchronization in the maintenance view.
- Filters synchronization targets to motors with the same parameter profile and
  synchronizes only writable, selected values or all safe writable values.
- Pre-reads the target, writes only differences, verifies each write, and saves
  the target through the SDK while excluding Node-ID and CAN baud-rate changes.
- Includes the matching x86 SDK and updater in the signed update package.

## 0.1.16

- Corrects the byte order regression introduced in 0.1.15: SimHub compact
  Binary axis output uses big-endian bytes. The wrong decoding could map the
  midpoint close to full stroke and turn small changes into large position jumps.
- Keeps byte order fixed, preserves 8 bit and legacy input compatibility,
  and validates decoding and position mapping with the actual SimHub encoder.
- Recommended for users of 0.1.15. No configuration changes are required.

## 0.1.15

- Fixes incorrect decoding of valid 9-16 bit SimHub binary axis values.
  Binary input now consistently follows the specified little-endian format,
  preventing position changes from switching the detected byte order.
- Preserves 8 bit, legacy text, and comma-separated binary input support.
- Includes the matching x86 SDK and versioned updater in the signed update
  package. Existing configuration is retained; no parameter changes are needed.

The little-endian assumption in 0.1.15 was incorrect for SimHub compact Binary
output and is superseded by 0.1.16.

## 0.1.14

- Adds a configurable CAN idle-disable timeout to the SimHub plugin.
- Defaults the timeout to 60 seconds after UDP timeout parking and disconnect;
  entering `0` disables SDK idle disable.
- Keeps initial CAN connection gated by the first valid UDP frame.

## 0.1.13

- Refreshes the bundled x86 `RaceBearSDK.dll` from the current SDK `0.6.0`
  Win32 Release build.
- Keeps the signed manifest, safe output shutdown, updater rollback, and
  normal SimHub exit flow from `0.1.12`.

## 0.1.12

- Version-only release for testing the hardened online update workflow from
  installed version 0.1.11.
- Retains signed package verification, safe output shutdown, and durable
  update transaction recovery introduced in 0.1.11.
- Uses the same update signing key and matching x86 SDK as 0.1.11.

## 0.1.11

- Adds RSA-3072/SHA-256 signed update manifests and strict package file
  verification.
- Adds durable updater journal recovery with complete rollback after
  interrupted or partially applied replacements.
- Requires the plugin to prepare a safe output shutdown before SimHub exits
  and requires deployment to wait for all target files to become unlocked.

## 0.1.10

- Separates maintenance controls and motor status into stable layout columns.
- Prevents the target, baud-rate, and status texts from overlapping in narrow windows.

## 0.1.9

- Displays Hardware, Software, and Bootloader Version as unsigned 32-bit values.
- Preserves the raw signed integer representation when writing version parameters.

## 0.1.8

- Places CAN Baud Rate directly below Node ID in the motor parameter list.
- Requires Node ID and CAN Baud Rate to be explicitly checked before writing.
- Keeps both communication-sensitive parameters excluded from “write all” by default.
- Adds 500K/1000K host baud-rate selection to the maintenance view.

## 0.1.7

- Routes update-check failures and in-progress warnings to the runtime log.
- Keeps routine device, binding, and validation feedback nonmodal.
- Retains dialogs only for explicit confirmations and blocking errors.

## 0.1.6

- Routes routine operation results to the runtime log instead of modal dialogs.
- Logs device refresh, binding, logical-index, and firmware validation issues.
- Keeps confirmation dialogs only for license deactivation and firmware updates.
- Keeps modal dialogs for update failures and other blocking errors.

## 0.1.5

- Moves the license action beside the activation-code input.
- Shows `Activate` when the SDK has no active license and `Deactivate` for a
  valid perpetual or timed license.
- Confirms device deactivation before submitting `license.deactivate`.

## 0.1.4

- Makes all three data-grid headers static and non-focusable.
- Disables column-header mouse interaction, keyboard focus, and sorting.
- Reduces all text input fields to a compact 22-pixel height.

## 0.1.3

- Right-aligns form labels and keeps related inputs close to their labels.
- Uses compact widths and left alignment for short text and selection fields.
- Tightens actuator stroke controls and other dense maintenance controls.
- Matches device, slave, and parameter list backgrounds to the runtime log.

## 0.1.2

- Runs the independent updater as a Windows application without a console window.
- Displays live package download progress and percentage in the plugin footer.
- Retains SHA-256, safe archive extraction, version matching, backup, and rollback checks.

## 0.1.1

- Adds current and latest plugin version information to the settings footer.
- Checks the fixed public GitHub repository for newer stable Releases.
- Downloads only the expected Win32 package and checksum assets.
- Verifies HTTPS hosts, SHA-256, archive paths, and assembly versions.
- Applies updates after SimHub exits through an independent updater.
- Backs up both plugin and SDK DLLs and rolls back failed replacement.

This is the first public online-update release. The installed `0.1.0`
baseline is retained for the end-to-end update test.

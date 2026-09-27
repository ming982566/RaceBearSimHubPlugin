# Release Notes

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

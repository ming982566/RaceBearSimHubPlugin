# Release Notes

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

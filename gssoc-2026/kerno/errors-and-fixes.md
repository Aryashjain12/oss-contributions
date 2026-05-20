# Errors and Fixes

## Error
undefined: unix.Timespec

## Cause
Kerno depends on Linux kernel APIs and eBPF tooling which are unavailable in native Windows builds.

## Fix
Switched testing workflow to WSL Ubuntu.

---

## Error
Go worked in PowerShell but not VSCode terminal.

## Cause
VSCode terminal environment was not refreshed after PATH updates.

## Fix
Restarted VSCode.
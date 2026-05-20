# Kerno Setup

## Environment
- Windows + WSL Ubuntu
- VSCode
- Go installed inside WSL

## Initial Setup
1. Forked Kerno repository
2. Cloned repository in WSL
3. Installed Go dependencies
4. Ran CLI tests

## Important Learning
Kerno depends on Linux/eBPF features, so development and tests should run inside WSL instead of native Windows PowerShell.

## Commands Used
go test ./internal/cli/
git checkout -b test-cli-flag-wiring
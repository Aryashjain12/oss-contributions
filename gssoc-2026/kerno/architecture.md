# Kerno Architecture Notes

## Important Directories

### internal/cli
Contains Cobra CLI commands and CLI tests.

### internal/bpf
Contains eBPF tracing logic.

### internal/chaos
Contains chaos engineering related modules.

## Observations
- Cobra framework used for CLI commands.
- Tests are organized feature-wise.
- Existing test files are useful references for new contributions.
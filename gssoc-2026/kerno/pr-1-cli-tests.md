# PR 1 — CLI Flag Wiring Tests

## Issue
Added missing flag wiring tests for:
- kerno trace disk
- kerno watch fd
- kerno watch oom

## Goal
Verify:
- flags exist
- defaults are correct
- shorthand flags work properly

## What I Learned
- Cobra flag registration
- Go CLI testing structure
- Existing OSS code adaptation workflow
- Shorthand flags using VarP methods

## Problems Faced
- Tests failed on Windows PowerShell
- Linux-specific APIs caused build errors

## Fix
Moved development/testing workflow to WSL Ubuntu.

## PR Workflow
1. Explored existing tests
2. Adapted doctor flag tests
3. Created new test files
4. Ran tests in WSL
5. Opened PR
6. Passed CI checks

## Key Engineering Lesson
Most OSS work involves understanding and adapting existing patterns rather than writing everything from scratch.

## Link
https://github.com/optiqor/kerno/pull/90cd 
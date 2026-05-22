# Issue #226 — Information Exposure via Verbose Exception Messages

## Problem
The API was returning raw exception messages using:

detail=str(e)

This could expose:
- internal file paths
- database details
- backend implementation details

## Goal
Replace unsafe exception exposure with:
- internal logging
- generic user-facing messages

## My Fix
- added Python logging
- added logger.exception(...)
- replaced detail=str(e)
- preserved rollback logic in batch endpoint

## Key Learning
- difference between ValueError and Exception
- why rebasing matters
- resolving merge conflicts
- secure API error handling
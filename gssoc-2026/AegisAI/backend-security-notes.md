Purpose:
## General reusable backend security knowledge.

NOT issue-specific.

Think:
> “What security concepts did I learn overall?”

This becomes your backend security handbook.

---

# WHAT TO WRITE

```md id="m2mdwl"
# Backend Security Notes

# Information Exposure

## Definition
Information exposure happens when backend systems reveal sensitive internal details to users or attackers.

---

# Common Causes

- returning raw exceptions
- stack trace leakage
- verbose debug responses
- SQL error exposure
- filesystem path disclosure

---

# Vulnerable Pattern

```python
detail=str(e)

# Secure Pattern
logger.exception("Internal failure")

raise HTTPException(
    status_code=500,
    detail="Internal server error"
)


FastAPI uses:
HTTPException
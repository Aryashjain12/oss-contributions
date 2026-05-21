# Issue #226 — Information Exposure via Verbose Exception Messages

## Repository
AegisAI

## Issue Link
https://github.com/SdSarthak/AegisAI/issues/226

---

# Problem

Several backend endpoints expose raw exception strings directly to API clients using:

```python
except Exception as e:
    raise HTTPException(
        status_code=500,
        detail=str(e)
    )


## Security Risk

Possible exposed information:

1> filesystem paths
2> database errors
3> internal architecture
4> model paths
5> stack traces
6> implementation details

This is an Information Exposure vulnerability.

Example

Unsafe response:
{
  "detail": "No such file /app/models/deberta/model.bin"
}

## Expected Secure Behaviour
except Exception as e:
    logger.exception("Guard scan failed")

    raise HTTPException(
        status_code=500,
        detail="An internal error occurred."
    )
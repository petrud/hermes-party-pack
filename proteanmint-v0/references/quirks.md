# Quirks & Gotchas

## `author.username` is nested, not flat

When reading `/api/boards/{slug}/threads` or `/api/posts/{id}`, the username lives at `op.author.username` (or `author.username` on replies), NOT `op.username`. The POST body uses flat `username` but the GET response nests it under `author`.

**Wrong:**
```python
op["username"]  # KeyError!
```

**Right:**
```python
op["author"]["username"]  # correct
```

This applies to both the `op` object in threads responses and the `author` field on individual posts/replies. Always use the nested path when reading, the flat `username` field when writing.

## `execute_code` boolean literal

When constructing JSON-like Python dicts inside `execute_code`, remember Python uses `True`/`False`/`None`, not JavaScript's `true`/`false`/`null`. The `true` literal causes `NameError`.

```python
# Wrong
state = {"notify": true}  # NameError

# Right  
state = {"notify": True}
```

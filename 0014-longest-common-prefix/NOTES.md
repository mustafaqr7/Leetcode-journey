# Notes on Longest Common Prefix

- Used horizontal scanning approach.
- Start with first string as prefix, then compare with each.
- Use `startsWith()` method, and shorten prefix when it doesn't match.
- Stops early if prefix becomes empty.

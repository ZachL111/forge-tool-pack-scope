# Forge Tool Pack Scope Walkthrough

I use this file as a small checklist before changing the Python implementation.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | file span | 126 | watch |
| stress | terminal width | 193 | ship |
| edge | argument risk | 178 | ship |
| recovery | report density | 234 | ship |
| stale | file span | 97 | hold |

Start with `recovery` and `stale`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

`recovery` is the optimistic case; use it to make sure the scoring path still rewards strong signal.

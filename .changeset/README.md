# Changesets

Every change that alters the font (outlines, metrics, features, names) is
described by a **changeset**: a small Markdown file in this directory. The
release automation collects them, picks the highest bump level, regenerates
`sources/`, writes `CHANGELOG.md` and opens the release pull request. The whole
flow is described in
[RELEASING.md](https://github.com/OctalMesh/OctalFont/blob/release/RELEASING.md).

## Add one

```sh
octalfont release add
```

```md
---
"octalfont-titan": minor
---

Tighten the spacing of the digits.
```

Font versions are `MAJOR.MINOR` with a three-digit minor:

| Level           | Result             | Use it for                                      |
|-----------------|--------------------|-------------------------------------------------|
| `minor`         | `1.000` -> `1.001` | Fixes, spacing and kerning, small additions     |
| `major`         | `1.012` -> `2.000` | A redesign or a new glyph set                   |
| `patch` (alias) | same as `minor`    | Accepted because other repositories use `patch` |

## Nothing to release?

Documentation, CI and README changes need no new version:

```sh
octalfont release add --empty
```

Do not edit `version` in `sources/font.yaml` or `CHANGELOG.md` by hand.

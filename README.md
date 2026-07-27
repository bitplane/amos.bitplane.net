# amos.bitplane.net

The published [amos-ts](https://github.com/bitplane/amos-ts) AMOS Professional
player. **This repository is a deploy target — do not hand-edit the site.**

Everything served here is built and pushed by CI from `bitplane/amos-ts` when a
`v*` tag lands. `main` holds only this README and the CNAME; the site itself
lives on the `release` branch, which GitHub Pages serves.

## Layout

```
/                     landing page and the standalone player
/v/<x.y.z>/           one published version, immutable
/v/latest/            the most recent release, moving
```

Versions are **paths, not query parameters** — a URL identifies exactly which
code runs, so a page can pin a version and cache it forever, and anyone can
reference a build that will not change under them.

## Embedding

Load the bundle from a versioned path and drive it from your own page; the
player never fetches your content, you hand it the bytes. Pin `/v/<x.y.z>/` if
you want it to stay put, or point at `/v/latest/` to pick up improvements.

## Licence

The player is MIT, same as amos-ts. AMOS Professional itself was Europress's;
this is a reimplementation, not a redistribution — no Amiga ROM and no AMOS
binaries are served from here.

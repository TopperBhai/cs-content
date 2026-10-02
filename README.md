# CS Launcher — Storefront content

This repo holds the **public storefront** for CS Launcher. It contains no source
code and no secrets.

```
content/catalogue.json      what is for sale (id, name, price, rarity, active)
content/catalogue.json.sig  Ed25519 signature of catalogue.json
content/capes/<id>.png      64x32 cape textures
```

## Do not edit by hand

Every file here is written by the **Cape Vault Admin** panel
(`CS Launcher.exe --admin`). The app verifies the signature on download and
ignores an unverified catalogue, so manual edits will simply be rejected.

## Why this repo is public

Players have to see prices without logging in, and a desktop app must never ship
an API token. So the *catalogue* is public while the *source* repo stays private.
What is on sale is protected by the signature, not by secrecy.

Published by the owner with a `repo`-scoped personal access token.

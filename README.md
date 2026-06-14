# SM-X110 / gta9wifi ROM Workspace

GitHub-ready project layout for Samsung Galaxy Tab A9 WiFi (`SM-X110`, `gta9wifi`) with clear separation between:

- source-side GSI patch materials
- device documentation
- flashable release assets

## Device snapshot

- **Model:** `SM-X110`
- **Codename:** `gta9wifi`
- **Platform:** `mt8781` (MediaTek Helio G99 family)
- **Stock Android observed:** 15
- **Dynamic partitions:** enabled

## Quick navigation

- `BUILDING.md` — build the GSI from source + patches
- `FLASHING.md` — flash-asset organization and safety notes
- `SOURCES.md` — inventory of source repos and artifacts
- `flash-assets/release-manifest.md` — canonical file list + SHA-256
- `COPY-CHECKLIST.md` — how to move local files into repo/release layout
- `PUBLISHING.md` — exact GitHub publish steps
- `releases/v1.0-beta-release-description.md` — copy-paste release text
- `releases/minimal-upload-set.md` — deduplicated upload matrix

## Repository structure

```text
SM-X110_GSI_Repo/
├── README.md
├── .gitattributes
├── .gitignore
├── BUILDING.md
├── FLASHING.md
├── SOURCES.md
├── COPY-CHECKLIST.md
├── PUBLISHING.md
├── docs/
├── source-patches/
├── flash-assets/
├── scripts/
└── releases/
```

## Important distinction

- A **source repo** contains buildable code and patch flow.
- A **release repo** contains prebuilt `.img`/`.tar` assets.

This workspace supports both, but keeps them separated to avoid mix-ups and bootloop roulette.

## Current status

- source patch bundle verified
- flash assets verified with checksums
- publish scaffold completed

If you’re starting fresh, use this order:

1. Read `SOURCES.md`
2. Read `BUILDING.md` or `FLASHING.md` depending on your goal
3. Follow `COPY-CHECKLIST.md`
4. Publish with `PUBLISHING.md`

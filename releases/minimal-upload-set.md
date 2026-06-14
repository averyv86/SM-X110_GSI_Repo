# Minimal Upload Set (Deduplicated)

This file proposes the smallest practical upload sets using your verified checksums.

## Why deduplication matters

Several files are byte-identical under different names, so uploading both adds size but no new content.

## Confirmed duplicate-equivalent pairs

- `system.img` == `system_pixel_chrome.img`
- `vbmeta.img` == `vbmeta_disabler.img`
- `system.tar` copies are identical
- `vbmeta.tar` copies are identical
- `vbmeta_system.img` copies are identical

(See `flash-assets/release-manifest.md` for exact SHA-256 values.)

## Recommended set A: Odin-first (tar workflow)

Upload these as your **primary** release assets:

1. `recovery.tar`
2. `system.tar`
3. `vbmeta.tar`
4. `vbmeta_system.img`

### Why this set

- Aligns with Odin-centric workflows using tar packages
- Smallest publish set for that method
- Avoids duplicate img/tar pairs where possible

## Recommended set B: IMG-first (recovery/fastbootd workflow)

Upload these if you want a raw image workflow:

1. `recovery_orangefox_fixed.img`
2. `system.img` (or `system_pixel_chrome.img`, choose one only)
3. `vbmeta_disabler.img` (or `vbmeta.img`, choose one only)
4. `vbmeta_system.img`

## Optional source artifact

Include only if you want reproducibility breadcrumbs in the release page:

- `LineageOS_gsi-2026.05.24-lineage23.2.zip`

## Naming recommendation

Use one naming convention per release to avoid confusion:

- Prefer `system.img` over `system_pixel_chrome.img` (or vice versa), but not both
- Prefer `vbmeta_disabler.img` over `vbmeta.img` (or vice versa), but not both

## Suggested GitHub release assets (simple)

If you want one clean, minimal release for most users, publish:

- `recovery.tar`
- `system.tar`
- `vbmeta.tar`
- `vbmeta_system.img`
- `SHA256SUMS.txt` (optional, generated from manifest)

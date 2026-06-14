# Building the GSI

This project uses a **source patch bundle** rather than a full device-specific ROM tree.

## Source bundle identified

- `LineageOS_gsi-2026.05.24-lineage23.2.zip`

This archive contains:

- `patches/apply-patches.sh`
- TrebleDroid / Lineage patch sets
- README instructions for building a Lineage 23.2 GSI

## Build type

This builds a **Treble GSI system image**, not a full `SM-X110` device ROM from scratch.

## Required environment

- Linux or WSL2 Ubuntu
- Java 17
- `repo`, `git`, `git-lfs`, `ccache`
- ~250 GB free disk space recommended

## High-level build flow

1. Initialize LineageOS source:
   - `repo init -u https://github.com/LineageOS/android.git -b lineage-23.2 --git-lfs`
2. Add treble manifest:
   - `git clone https://github.com/MisterZtr/treble_manifest.git .repo/local_manifests -b lineage-23.2`
3. Sync source
4. Extract the GSI patch bundle
5. Run `patches/apply-patches.sh`
6. Build `systemimage`

## Recommended first target

Use the vanilla ext4 target first:

- `lineage_arm64_bvN4-bp4a-userdebug`

## Expected output

Usually:

- `out/target/product/tdgsi_arm64_ab/system.img`

## Important note

This repo currently documents the build process, but does not yet contain the full Android source checkout.

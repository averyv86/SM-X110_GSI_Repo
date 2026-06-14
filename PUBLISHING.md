# Publish to GitHub

This guide publishes the scaffolded project and prepares release assets.

## 1) Initialize local git repository

Use these commands in the repo root (`C:\Users\avery\Desktop\SM-X110_GSI_Repo`):

- `git init`
- `git add .`
- `git commit -m "Initial SM-X110 GSI project scaffold"`

## 2) Create GitHub repository

Create an empty repository on GitHub, then link it:

- `git remote add origin https://github.com/<your-user>/<your-repo>.git`
- `git branch -M main`
- `git push -u origin main`

## 3) (Optional) Enable Git LFS

If storing large binaries in-repo:

- `git lfs install`
- `git lfs track "*.img" "*.tar" "*.xz" "*.zip"`
- `git add .gitattributes`
- `git commit -m "Enable Git LFS tracking for release binaries"`
- `git push`

## 4) Recommended release flow

Preferred approach for large files:

1. Keep docs/manifests in git
2. Upload `.img` and `.tar` files to GitHub Releases
3. Include checksums from `flash-assets/release-manifest.md`
4. Add concise flash notes in release description

## 5) Suggested tags

- `v1.0-beta` for current baseline package
- `v1.0` after confirmed stable flash set

## 6) Suggested release notes template

- Device: `SM-X110` (`gta9wifi`)
- Base: LineageOS/treble GSI package details
- Included assets: recovery/system/vbmeta list
- SHA-256 checksums: link to `flash-assets/release-manifest.md`
- Known issues and rollback notes

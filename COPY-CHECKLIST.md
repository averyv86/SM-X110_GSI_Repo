# Copy Checklist (Local Files -> Repo Layout)

Use this checklist to move your current files into a clean GitHub structure.

## Source-side bundle

- [ ] Copy `C:\Users\avery\Downloads\LineageOS_gsi-2026.05.24-lineage23.2.zip`
      -> `source-patches\LineageOS_gsi-2026.05.24-lineage23.2.zip`

## Flash assets (documentation-first approach)

Recommended: keep binaries in GitHub Releases and store only manifests/docs in git.

If you still want local staging under this repo:

- [ ] `C:\Users\avery\Desktop\Flash_Me\system.img`
      -> `flash-assets\system.img`
- [ ] `C:\Users\avery\Desktop\Flash_Me\system.tar`
      -> `flash-assets\system.tar`
- [ ] `C:\Users\avery\Desktop\Flash_Me\vbmeta.img`
      -> `flash-assets\vbmeta.img`
- [ ] `C:\Users\avery\Desktop\Flash_Me\vbmeta.tar`
      -> `flash-assets\vbmeta.tar`
- [ ] `C:\Users\avery\Desktop\Flash_Me\vbmeta_disabled_custom.img`
      -> `flash-assets\vbmeta_disabled_custom.img`
- [ ] `C:\Users\avery\Desktop\Flash_Me\vbmeta_system.img`
      -> `flash-assets\vbmeta_system.img`
- [ ] `C:\Users\avery\Desktop\Flash_Me\recommended_img_files\recovery.tar`
      -> `flash-assets\recovery.tar`
- [ ] `C:\Users\avery\Desktop\Flash_Me\recommended_img_files\recovery_orangefox_fixed.img`
      -> `flash-assets\recovery_orangefox_fixed.img`
- [ ] `C:\Users\avery\Desktop\Flash_Me\recommended_img_files\system_pixel_chrome.img`
      -> `flash-assets\system_pixel_chrome.img`
- [ ] `C:\Users\avery\Desktop\Flash_Me\recommended_img_files\vbmeta_disabler.img`
      -> `flash-assets\vbmeta_disabler.img`

## Release metadata

- [ ] Keep `flash-assets\release-manifest.md` updated with final checksum values
- [ ] Add changelog entry under `releases\`
- [ ] Upload large artifacts to GitHub Release assets

## Final sanity checks

- [ ] Filenames are consistent (`system.img` vs `system_pixel_chrome.img` clearly documented)
- [ ] No Qualcomm/Snapdragon references for this MediaTek device
- [ ] Checksums match exactly before publishing

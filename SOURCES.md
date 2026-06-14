# Source and Asset Inventory

## Source-oriented materials

### GSI patch bundle

- File: `LineageOS_gsi-2026.05.24-lineage23.2.zip`
- Local path: `C:\Users\avery\Downloads\LineageOS_gsi-2026.05.24-lineage23.2.zip`
- Type: Source patch bundle
- Purpose: Apply patches onto a full LineageOS 23.2 + Treble source checkout, then build a GSI `system.img`

## Device/release repositories reviewed

### Device tree repository

- Repo: `https://github.com/averyv86/android_device_samsung_gta9wifi`
- Type: Device tree source repository
- Contains: `BoardConfig.mk`, `device.mk`, `AndroidProducts.mk`, overlays, configs, sepolicy
- Missing for a full end-to-end build: vendor tree, kernel tree, full Android source checkout

### Release/tools repository

- Repo: `https://github.com/averyv86/SamsungPixelOS_Tools`
- Type: Release/distribution repository
- Contains: README + release asset references
- Does not contain full build source

## Flash asset locations

### Main folder

- `C:\Users\avery\Desktop\Flash_Me`

### Recommended image folder

- `C:\Users\avery\Desktop\Flash_Me\recommended_img_files`

## Conclusion

You currently have enough material to:

- document a GitHub project clearly
- publish release assets cleanly
- attempt GSI flashing workflows

You do **not** yet have a complete full-ROM reproducible source tree in this repo.

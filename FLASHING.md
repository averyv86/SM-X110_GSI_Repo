# Flashing Notes for SM-X110 / gta9wifi

## Device facts confirmed

- Model: `SM-X110`
- Codename: `gta9wifi`
- Platform: `mt8781`
- Dynamic partitions: enabled

## Observed partitions

The connected device exposes at least:

- `boot`
- `init_boot`
- `vendor_boot`
- `dtbo`
- `vbmeta`
- `vbmeta_system`
- `vbmeta_vendor`
- `recovery`
- `super`

## Current local flash assets

From `C:\Users\avery\Desktop\Flash_Me` and `recommended_img_files`:

- `system.img`
- `system.tar`
- `vbmeta.img`
- `vbmeta.tar`
- `vbmeta_system.img`
- `vbmeta_disabled_custom.img`
- `recovery.tar`
- `recovery_orangefox_fixed.img`
- `vbmeta_disabler.img`

## Suggested release organization

### Recovery assets

- `recovery.tar`
- `recovery_orangefox_fixed.img`

### VBMeta assets

- `vbmeta.tar`
- `vbmeta.img`
- `vbmeta_disabler.img`
- `vbmeta_system.img`

### System assets

- `system.img`
- `system.tar`
- `system_pixel_chrome.img`

## Safety notes

- Verify the device is really `SM-X110`
- Do not flash Qualcomm-targeted images on this MediaTek tablet
- Dynamic partition devices often rely on correct vbmeta handling
- Recovery, vbmeta, and system images should be treated as a matched set when possible

## Not yet verified here

This documentation does **not** prove boot success for every provided image combination. It only organizes the known files and device facts.

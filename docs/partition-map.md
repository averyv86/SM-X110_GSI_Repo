# Partition Map

## Observed partitions from connected device

- `boot`
- `init_boot`
- `vendor_boot`
- `dtbo`
- `vbmeta`
- `vbmeta_system`
- `vbmeta_vendor`
- `recovery`
- `super`
- `userdata`

## Notes

This appears to be a dynamic-partition Samsung/MediaTek layout. That means a GSI workflow is generally more realistic here than pretending this is already a full device-specific ROM source tree.

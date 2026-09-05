# Realme Even (RMX3195) — CherishOS (Android 14 / RUI4) Manifest

## Build Instructions

```bash
# Initialize CherishOS 14 manifest
repo init -u https://github.com/CherishOS/android_manifest.git -b fourteen --git-lfs

# Clone device manifest
git clone -b cherish-a14 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

# Sync source
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

# Build
source build/envsetup.sh
lunch cherish_even-eng
mka bacon -j$(nproc)
```

## Branches Used

| Component | Branch |
|-----------|--------|
| Device tree | `cherish-a14-rui4` (RUI4 fork) |
| Vendor blobs | `cherish-a14-rui4` (RUI4 fork) |
| Kernel | Zenium `rui4-clean` |
| MTK HALs | `lineage-21` |
| MTK sepolicy | `lineage-21` |
| Pocket Mode | `UNO` |

## Notes

- Uses RUI4 (Android 14) device/vendor trees — separate from RUI2 repos
- Uses Zenium kernel (not stock MTK)
- Removes all Qualcomm/Google packages (MTK device)

# Realme Even (RMX3195) — RisingOS A16 Manifest

## Build Instructions

```bash
# Initialize RisingOS manifest
repo init -u https://github.com/RisingOS-Revived/android_manifest.git -b sixteen-qpr2 --git-lfs

# Clone device manifest
git clone -b rising-a16 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

# Sync source
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

# Build
source build/envsetup.sh
lunch <target>
mka bacon -j$(nproc)
```

## Branches Used

| Component | Branch |
|-----------|--------|
| Device tree | `risingos-a16` (RUI4 fork) |
| Vendor blobs | `risingos-a16` (RUI4 fork) |
| Kernel | Zenium `rui4-clean` |
| IMS | `thirteen` (RMX3191-ims) |
| RisingOS vendor | `sixteen-qpr2` |
| RisingOS lineage | `sixteen-qpr2` |
| Toolchain | zyc clang 14 |

## Notes

- Uses RUI4 (Android 16) device/vendor trees
- Uses Zenium kernel
- RisingOS Settings replaces LineageOS Settings (has Personalizations customization)
- Removes vendor/gms from default manifest

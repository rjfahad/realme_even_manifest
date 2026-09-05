# Realme Even (RMX3195) — LineageOS 20 Manifest

## Build Instructions

```bash
# Initialize LineageOS 20 manifest
repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs

# Clone device manifest
git clone -b los-20 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

# Sync source
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

# Build
source build/envsetup.sh
lunch lineage_even-eng
mka bacon -j$(nproc)
```

## Branches Used

| Component | Branch |
|-----------|--------|
| Device tree | `los-20` |
| Vendor blobs | `los-20` |
| IMS | `thirteen` (RMX3191-ims) |
| Kernel | `los-20` |
| MTK HALs | `lineage-20` |
| MTK sepolicy | `lineage-20` |
| Toolchain | zyc clang 14 |
| RealmeParts | `lineage-20-fps` |
| Trebuchet | `lineage-20.0-ram` (RAM info in recents) |

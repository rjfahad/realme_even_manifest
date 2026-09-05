# Realme Even (RMX3195) — LineageOS 21 Manifest

## Build Instructions

```bash
# Initialize LineageOS 21 manifest
repo init -u https://github.com/LineageOS/android.git -b lineage-21.0 --git-lfs

# Clone device manifest
git clone -b los-21 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

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
| Device tree | `los-21` |
| Vendor blobs | `los-21` |
| IMS | `fourteen` (RMX3191-ims) |
| Kernel | `los-21` |
| MTK HALs | `lineage-21` |
| MTK sepolicy | `lineage-21` |
| Oplus HALs | `lineage-21` |
| Toolchain | zyc clang 14 |
| RealmeParts | `lineage-21` |
| Pocket Mode | `UNO` |

# Realme Even (RMX3195) — ArrowOS 13 Manifest

## Build Instructions

```bash
# Initialize ArrowOS 13 manifest
repo init -u https://github.com/ArrowOS/android_manifest.git -b arrow-13.0 --git-lfs

# Clone device manifest
git clone -b arrow-13.0 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

# Sync source
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

# Build
source build/envsetup.sh
lunch even-user
mka bacon -j$(nproc)
```

## Branches Used

| Component | Branch |
|-----------|--------|
| Device tree | `arrow-13.0` (based on los-20) |
| Vendor blobs | `arrow-13.0` (based on los-20) |
| IMS | `sixteen-qpr1` (RMX2020-ims) |
| Kernel | `los-20` |
| MTK HALs | `lineage-20` |
| MTK sepolicy | `lineage-20` |
| Toolchain | zyc clang 14 |
| RealmeParts | `lineage-20-fps` |

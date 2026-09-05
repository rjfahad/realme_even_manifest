# Realme Even (RMX3195) — CherishOS (Android 13) Manifest

## Build Instructions

```bash
# Initialize CherishOS manifest
repo init -u https://github.com/CherishOS/android_manifest.git -b tiramisu --git-lfs

# Clone device manifest
git clone -b cherish https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

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
| Device tree | `cherish` |
| Vendor blobs | `cherish` |
| IMS | `sixteen-qpr1` (RMX3191-ims) |
| Kernel | `los-20` |
| Toolchain | zyc clang 14 |
| RealmeParts | `lineage-20-fps` |

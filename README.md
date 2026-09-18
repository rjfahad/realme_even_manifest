# Realme Even (RMX3191) — crDroid 13 Manifest

Vanilla (non-GMS) by default.

## Build Instructions

```bash
# Initialize crDroid 13 manifest
repo init -u https://github.com/crdroidandroid/android.git -b 13.0 --git-lfs

# Clone device manifest
git clone -b crdroid-13.0 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

# Sync source
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

# Build
source build/envsetup.sh
lunch lineage_even-userdebug
m bacon -j$(nproc)
```

## Branches Used

| Component | Repo | Branch |
|-----------|------|--------|
| Device tree | `rjfahad/device_realme_even` | `crdroid-13.0` (los-20 base) |
| Vendor blobs | `rjfahad/vendor_realme_even` | `crdroid-13.0` (los-20 base) |
| IMS | `rjfahad/vendor_realme_RMX3191-ims` | `thirteen` |
| Kernel | `rjfahad/kernel_realme_even` | `los-20` |
| MTK HALs | `LineageOS/android_hardware_mediatek` | `lineage-20` |
| MTK sepolicy | `LineageOS/android_device_mediatek_sepolicy_vndr` | `lineage-20` |
| Toolchain | `greenforce-project/greenforce_clang` | `main` (Greenforce Clang 24) |
| RealmeParts | `rjfahad/android_packages_apps_RealmeParts` (fork of HyperTeam) | `lineage-20-fps` |

Note: per upstream crDroid convention there is no separate `crdroid_even.mk` —
`lineage_even.mk` is the single product entry point (`PRODUCT_NAME := lineage_even`).

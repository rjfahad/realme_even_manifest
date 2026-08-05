# Realme Even (RMX3191) — LineageOS 20 Manifest

```bash
repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs
git clone -b los-20 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

source build/envsetup.sh
lunch lineage_even-user
mka bacon -j$(nproc)
```

## Manifest Contents

| Component | Path | Branch |
|-----------|------|--------|
| Device tree | `device/realme/even` | `los-20` |
| Vendor blobs | `vendor/realme/even` | `los-20` |
| IMS | `vendor/realme/RMX3191-ims` | `thirteen` |
| Kernel | `kernel/realme/even` | `los-20` |
| MTK sepolicy | `device/mediatek/sepolicy_vndr` | `lineage-20` |
| MTK HALs | `hardware/mediatek` | `lineage-20` |
| Greenforce Clang | `prebuilts/clang/host/linux-x86/greenforce-clang` | `main` |
| RealmeParts | `packages/apps/RealmeParts` | `lineage-20-fps` |

## Toolchain

Greenforce Clang 24 is auto-downloaded on first build via `vendorsetup.sh`.

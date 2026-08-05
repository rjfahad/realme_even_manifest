# Realme Even (RMX3191) — SuperiorOS Extended Manifest

```bash
repo init -u https://github.com/SuperiorOS/manifest.git -b thirteen --git-lfs
git clone -b superrios-13.0 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

source build/envsetup.sh
lunch superior_even-user
mka bacon -j$(nproc)
```

## Manifest Contents

| Component | Path | Branch |
|-----------|------|--------|
| Device tree | `device/realme/even` | `superioros-13` |
| Vendor blobs | `vendor/realme/even` | `superioros-13` |
| IMS | `vendor/realme/RMX3191-ims` | `thirteen` |
| Kernel | `kernel/realme/even` | `los-20` |
| MTK sepolicy | `device/mediatek/sepolicy_vndr` | `lineage-20` |
| MTK HALs | `hardware/mediatek` | `lineage-20` |
| Greenforce Clang | `prebuilts/clang/host/linux-x86/greenforce-clang` | `main` |
| RealmeParts | `packages/apps/RealmeParts` | `lineage-20-fps` |

## Toolchain

Greenforce Clang 24 is auto-downloaded on first build via `vendorsetup.sh`.

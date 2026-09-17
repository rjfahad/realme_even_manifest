# Realme Even (RMX3191) — DerpFest A13 Manifest

```bash
repo init -u https://github.com/DerpFest-AOSP/manifest.git -b 13 --git-lfs
git clone -b derpfest-a13 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

source build/envsetup.sh
lunch derp_even-user
mka derp -j$(nproc)
```

## Manifest Contents

| Component | Path | Branch |
|-----------|------|--------|
| Device tree | `device/realme/even` | `derpfest-a13` |
| Vendor blobs | `vendor/realme/even` | `derpfest-a13` |
| IMS | `vendor/realme/RMX3191-ims` | `thirteen` |
| Kernel | `kernel/realme/even` | `los-20` |
| MTK sepolicy | `device/mediatek/sepolicy_vndr` | `lineage-20` |
| MTK HALs | `hardware/mediatek` | `lineage-20` |
| Greenforce Clang | `prebuilts/clang/host/linux-x86/greenforce-clang` | `main` |
| RealmeParts | `packages/apps/RealmeParts` | `lineage-20-fps` |

## Toolchain

Greenforce Clang 24 is auto-downloaded on first build via `vendorsetup.sh`.

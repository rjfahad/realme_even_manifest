# Realme Even (RMX3191) — CherishOS A14 Manifest

```bash
repo init -u https://github.com/CherishOS/android_manifest.git -b udc --git-lfs
git clone -b cherish-a14 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

source build/envsetup.sh
lunch cherish_even-user
mka bacon -j$(nproc)
```

## Manifest Contents

| Component | Path | Branch |
|-----------|------|--------|
| Device tree | `device/realme/even` | `cherish-a14-rui4` (RUI4) |
| Vendor blobs | `vendor/realme/even` | `cherish-a14-rui4` (RUI4) |
| Kernel | `kernel/realme/even` | `rui4-clean` (Zenium) |
| MTK sepolicy | `device/mediatek/sepolicy_vndr` | `lineage-21` |
| MTK HALs | `hardware/mediatek` | `lineage-21` |
| Pocket Mode | `packages/apps/PocketMode` | `UNO` |

# Realme Even (RMX3191) — RisingOS A16 Manifest

```bash
repo init -u https://github.com/RisingOS-Revived/android.git -b sixteen-qpr2 --git-lfs
git clone -b rising-a16 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

source build/envsetup.sh
lunch rising_even-user
mka bacon -j$(nproc)
```

## Manifest Contents

| Component | Path | Branch |
|-----------|------|--------|
| Device tree | `device/realme/even` | `risingos-a16` (RUI4) |
| Vendor blobs | `vendor/realme/even` | `risingos-a16` (RUI4) |
| Kernel | `kernel/realme/even` | `rui4-clean` (Zenium) |
| IMS | `vendor/realme/RMX3191-ims` | `thirteen` |
| RisingOS vendor | `vendor/rising` | `sixteen-qpr2` |
| RisingOS lineage | `vendor/lineage` | `sixteen-qpr2` |
| RisingOS Settings | `packages/apps/Settings` | `sixteen` |
| Toolchain | `prebuilts/clang/host/linux-x86/greenforce-clang` | `main) |

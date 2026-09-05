# Realme Even (RMX3195) — DerpFest 14 Manifest (Unmaintained)

## Build Instructions

```bash
# Initialize LineageOS 21 manifest (DerpFest is based on LOS 21)
repo init -u https://github.com/LineageOS/android.git -b lineage-21.0 --git-lfs

# Clone device manifest
git clone -b derp-14 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests

# Sync source
repo sync -c --no-tags --no-clone-bundle -j$(nproc)

# Build
source build/envsetup.sh
lunch <target>
mka bacon -j$(nproc)
```

## Branches Used

| Component | Branch |
|-----------|--------|
| Device tree | `derp-14-oss` (RMX3191) |
| Vendor blobs | `vendor-oss` |
| Vendor IMS | `vendor-oss` (even-ims) |
| Kernel | `ReSukiSU` (liquid kernel) |
| MTK HALs | `lineage-21` |
| MTK sepolicy | `lineage-21` |
| Oplus HALs | `lineage-21` |

## Notes

- **Unmaintained** — use at your own risk
- Uses OSS device/vendor trees (RMX3191 path)
- All source-built HALs (no prebuilt blobs)

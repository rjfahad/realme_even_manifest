# Realme Even (RMX3191) — ROM Build Manifests

Local manifests for building custom ROMs for Realme Even (RMX3191/RMX3195, MT6768).

## Branches

| Branch | ROM | Android | Extras |
|--------|-----|---------|--------|
| `los-20` | LineageOS 20 | 13 | Trebuchet (RAM info), RealmeParts (FPS overlay, HBM, OTG, Game Mode), QUIK messaging |
| `los-21` | LineageOS 21 | 14 | RealmeParts (FPS overlay, HBM, OTG, Game Mode), Pocket Mode |
| `crdroid` | crDroid | 13 | RealmeParts (FPS overlay) |
| `cherish` | CherishOS | 13 | RealmeParts (FPS overlay, HBM, OTG, Game Mode) |
| `cherish-a14` | CherishOS | 14 | **RUI4** device/vendor/kernel, **Zenium** kernel (rui4-clean), RealmeParts, Pocket Mode, Dolby |
| `derp-14` | DerpFest 14 | 14 | *(unmaintained)* |
| `rising-a16` | RisingOS Revived | 16 QPR2 | **RUI4** (`device_realme_even_rui4`), **Zenium** (`rui4-clean`), `vendor/rising`, Settings fork (Personalizations) |

## Usage

### RisingOS Revived (rising-a16)

```bash
repo init -u https://github.com/RisingOS-Revived/android.git -b sixteen-qpr2 --git-lfs
git clone -b rising-a16 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

### LineageOS / CherishOS / crDroid

```bash
repo init -u https://github.com/LineageOS/android.git -b lineage-20.0 --git-lfs
git clone -b los-20 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

Replace `-b los-20` with the desired branch (`los-21`, `crdroid`, `cherish`, `cherish-a14`, `derp-14`).

For CherishOS (Android 14):
```bash
repo init -u https://github.com/CherishOS/android_manifest.git -b fourteen --git-lfs
git clone -b cherish-a14 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```
Uses **RUI4** device/vendor/kernel, **Zenium** kernel, RealmeParts, Pocket Mode, Dolby, and LineageOS 21 HALs.

Or copy `roomservice.xml` manually:

```bash
mkdir -p .repo/local_manifests
cp roomservice.xml .repo/local_manifests/
```

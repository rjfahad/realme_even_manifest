# Realme Even (RMX3191) — ROM Build Manifests

Local manifests for building custom ROMs for Realme Even (RMX3191/RMX3195, MT6768).

## Branches

| Branch | ROM | Android | Extras |
|--------|-----|---------|--------|
| `los-20` | LineageOS 20 | 13 | Trebuchet (RAM info), RealmeParts (FPS overlay, HBM, OTG, Game Mode), QUIK messaging |
| `los-21` | LineageOS 21 | 14 | RealmeParts (FPS overlay, HBM, OTG, Game Mode), Pocket Mode |
| `crdroid` | crDroid | 13 | RealmeParts (FPS overlay) |
| `sparkos` | SparkOS | 13 | RealmeParts (FPS overlay, HBM, OTG, Game Mode) |
| `cherish` | CherishOS | 13 | RealmeParts (FPS overlay, HBM, OTG, Game Mode) |
| `cherish-a14` | CherishOS | 14 | RealmeParts (FPS overlay, HBM, OTG, Game Mode), Zenium kernel (RUI4), PocketMode, Dolby |
| `derp-14` | DerpFest 14 | 14 | *(unmaintained)* |

## Usage

Clone the appropriate branch into `.repo/local_manifests` before running `repo sync`:

```bash
repo init -u https://github.com/LineageOS/android.git -b lineage-20.0
git clone -b los-20 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

Replace `-b los-20` with the desired branch (`los-21`, `crdroid`, `sparkos`, `cherish`, `cherish-a14`).

For SparkOS:
```bash
repo init -u https://github.com/Spark-Rom/manifest -b pyro-next
git clone -b sparkos https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

For CherishOS (Android 13):
```bash
repo init -u https://github.com/CherishOS/android_manifest.git -b tiramisu
git clone -b cherish https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

For CherishOS (Android 14):
```bash
repo init -u https://github.com/CherishOS/android_manifest.git -b fourteen
git clone -b cherish-a14 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

Or copy `roomservice.xml` manually:

```bash
mkdir -p .repo/local_manifests
cp roomservice.xml .repo/local_manifests/
```

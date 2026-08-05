# Realme Even (RMX3191) — ROM Build Manifests

Local manifests for building custom ROMs for Realme Even (RMX3191/RMX3195, MT6768).

## Branches

| Branch | ROM |
|--------|-----|
| `rising-14` | RisingOS 14 (fourteen) |
| `universal` | ROM-agnostic AOSP base |

## Usage

```bash
repo init -u https://github.com/RisingTechOSS/android.git -b fourteen --git-lfs
git clone -b rising-14 https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

Or copy manually:

```bash
mkdir -p .repo/local_manifests
cp .repo/local_manifests/roomservice.xml .repo/local_manifests/
```

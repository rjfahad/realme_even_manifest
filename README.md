# Realme Even (RMX3191) — ROM Build Manifests

Local manifests for building custom ROMs for Realme Even (RMX3191/RMX3195, MT6768).

## Branches

| Branch | ROM |
|--------|-----|
| `universal` | ROM-agnostic AOSP base |

## Usage

```bash
repo init -u https://github.com/DerpFest-AOSP/manifest.git -b 14 --git-lfs
git clone -b universal https://github.com/rjfahad/realme_even_manifest.git .repo/local_manifests
repo sync
```

Or copy manually:

```bash
mkdir -p .repo/local_manifests
cp .repo/local_manifests/roomservice.xml .repo/local_manifests/
```

# yetty-alpine-9p-fs

Alpine Linux 9P filesystem for JSLinux/TinyEMU.

## About

This repo builds a minimal Alpine Linux rootfs packaged as a 9P filesystem
for use with [yetty](https://github.com/user/yetty) WebAssembly builds.

The filesystem is deployed to GitHub Pages on each version tag.

## Building Locally

```bash
./build.sh dist
```

Output will be in `dist/` directory.

## Releases

Create a version tag to trigger a build and deploy:

```bash
git tag v1.0.0
git push origin v1.0.0
```

The GitHub Actions workflow builds and deploys to Pages on tags matching `vX.Y.Z`.

## Usage in yetty

Point yetty's JSLinux configuration to:
```
https://USER.github.io/yetty-alpine-9p-fs/
```

## build dependencies

1. `build-essentials` or equivalent: `make automake gcc gcc-c++ kernel-devel`

2. https://emscripten.org/docs/getting_started/downloads.html#linux

3. Follow the docs in docs/HACKING.md for creating a desktop build

```
npm ci
```

## Building

Download and install the latest SDK tools
```
./emsdk install latest
```
Make the "latest" SDK "active" for the current user. (writes .emscripten file)
```
./emsdk activate latest
```
# Activate PATH and other environment variables in the current terminal
`source ./emsdk_env.sh`

commence the build
```
node make --desktop-build-only prod
node desktop --custom-desktop-release
```

Copy the resulting AppImage to the desired location
```
cp artifacts/desktop/tutanota-desktop-linux.AppImage ~/Applications/Tutanota/
```
# Icon for Tipitakapali.org offline

- On a Mac, run:

```bash 
iconutil -c icns IconAssets.iconset -o icon.icns

```

It is used for Tipitakapali.org offline releases [here](https://github.com/tipitakapali/tipitakapali.org/releases
)

## Electron notes

- Icons for Electron apps, remember to put the `icon.icns` file to the `build` dir. Do not change name.

- The `license_en.txt` file is for showing license notes (when installing `dmg` files).

```text
.
├── main.js
├── package.json
├── build
│   ├── icon.icns
│   ├── icon.ico
│   ├── icon.png
│   ├── icons
│   │   ├── icon.icns
│   │   ├── icon.ico
│   │   ├── icon.png
│   │   ├── mac
│   │   │   └── icon.icns
│   │   ├── png
│   │   │   ├── 1024x1024.png
│   │   │   ├── 128x128.png
│   │   │   ├── 16x16.png
│   │   │   ├── 24x24.png
│   │   │   ├── 256x256.png
│   │   │   ├── 32x32.png
│   │   │   ├── 48x48.png
│   │   │   ├── 512x512.png
│   │   │   ├── 64x64.png
│   │   │   ├── icon_128@2x.png
│   │   │   ├── icon_128.png
│   │   │   ├── icon_16@2x.png
│   │   │   ├── icon_16.png
│   │   │   ├── icon_24@2x.png
│   │   │   ├── icon_24.png
│   │   │   ├── icon_256@2x.png
│   │   │   ├── icon_256.png
│   │   │   ├── icon_32@2x.png
│   │   │   ├── icon_32.png
│   │   │   ├── icon_512@2x.png
│   │   │   └── icon_512.png
│   │   ├── README.md
│   │   └── win
│   │       └── icon.ico
│   └── license_en.txt


```

Simplified package.json:

```json 

{
  "version": "24.7.20",
  "name": "tipitakapali.org",
  "main": "main.js",
  "scripts": {
    "build-mac": "bash mac_prepare.sh && electron-builder -m",
  },
  "build": {
    "asar": true,
    "asarUnpack": [
      "build/icons"
    ],
    "directories": {
      "buildResources": "build",
      "output": "dist"
    },
    "files": [
      "build/**/*",
      "main.js",
      other files to be included here
    ],
   ...
}

}

```

## Thanks

- The icon is generated with [http://tipitaka.app/misc/dhammachakka](http://tipitaka.app/misc/dhammachakka)

- Tut: https://bootcamp.uxdesign.cc/5-steps-to-create-a-macos-app-icon-in-icns-format-a659f27f1a85
# Lutris: Script

## Requirements

- A Linux distribution
- [Lutris](https://lutris.net), installed via Flatpak or native package
- [DWPROTON](https://dawn.wine/dawn-winery/dwproton)

## Runner Setup

### Option 1: ProtonPlus Or Another Third-Party Installer

1. Install ProtonPlus or another runner installer that supports Lutris.
2. Select Lutris as the target launcher if the installer asks.
3. Install **DW-Proton Latest** or the latest DW Proton release.
4. Restart Lutris.
5. Confirm DW Proton is available as a Wine runner.

### Option 2: Manual Download

Install Lutris and make sure DW Proton is available as the Wine runner you intend to use. The Script recommends `dwproton-10.0-20` for the script path.

## Prefix/Game Setup

Use the installer script below. It creates a 64-bit Wine prefix, downloads the NIKKE installer, runs it, and points Lutris to the launcher executable.

```yaml
description: "Installs GODDESS OF VICTORY: NIKKE official launcher. Recommended to use dwproton-10.0-20"
game_slug: nikke
gogslug: ''
humblestoreid: ''
installer_slug: nikke-installer
name: "GODDESS OF VICTORY: NIKKE"
notes: "Installs GODDESS OF VICTORY: NIKKE's launcher."
runner: wine
script:
  files:
    - nikkeinstaller:
        filename: nikkeminiloader0.0.6.346.exe
        url: https://nikke-en.com/nikkeminiloader0.0.6.346.exe
  game:
    exe: drive_c/NIKKE/Launcher/nikke_launcher.exe
    prefix: $GAMEDIR
  installer:
    - task:
        arch: win64
        name: create_prefix
        prefix: $GAMEDIR
    - task:
        description: "Install Goddess of Victory: NIKKE's launcher, then close the prompt once installation is complete.\nAvoid launching the game from the installer."
        executable: nikkeinstaller
        name: wineexec
        prefix: $GAMEDIR
        env:
          PROTON_VERB: run
  system:
    env:
      GAMEID: umu-nikke
slug: nikke-installer
steamid: null
version: Nikke Installer
year: 2023
```

## Install/Update Notes

1. Import or run the Lutris script.
2. Let the script create the prefix and run the official launcher installer.
3. Close the installer prompt once installation is complete.
4. Avoid launching the game directly from the installer.
5. Launch through Lutris using `drive_c/NIKKE/Launcher/nikke_launcher.exe`.

Updates should be handled through the launcher.

Shared troubleshooting lives in [known issues](../../known-issues.md).

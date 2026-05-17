# Steam: DW Proton

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Steam for Linux
- [DWPROTON](https://dawn.wine/dawn-winery/dwproton)

## Runner Setup

### Option 1: ProtonPlus Or Another Third-Party Installer

1. Install ProtonPlus or another compatibility-tool installer that supports Steam.
2. Select Steam as the target launcher if the installer asks.
3. Install **DW-Proton Latest** or the latest DW Proton release.
4. Restart Steam after installing DW Proton.
5. Confirm DW Proton appears under the non-Steam game's compatibility options.

### Option 2: Manual Download

1. Download the latest DW Proton release archive from [Dawn Winery](https://dawn.wine/dawn-winery/dwproton/releases).
2. Create Steam's custom compatibility tool directory if it does not exist:

   ```text
   Native Steam: ~/.steam/root/compatibilitytools.d/
   Flatpak Steam: ~/.var/app/com.valvesoftware.Steam/data/Steam/compatibilitytools.d/
   Snap Steam: ~/snap/steam/common/.steam/steam/compatibilitytools.d/
   ```

   On many native installs, `~/.steam/root/` and `~/.steam/steam/` point at the same Steam directory. Prefer `~/.steam/root/compatibilitytools.d/` unless your distro documents a different Steam root.

3. Extract the DW Proton archive into the matching `compatibilitytools.d` directory. Do not flatten the archive; Steam expects one runner folder under `compatibilitytools.d`.

   Example native layout:

   ```text
   ~/.steam/root/compatibilitytools.d/dwproton-<version>/
   ```

4. Check that the runner folder contains Steam compatibility tool files such as `compatibilitytool.vdf`, `proton`, and `toolmanifest.vdf`.
5. Restart Steam after installing DW Proton.
6. Confirm DW Proton appears under the non-Steam game's compatibility options.

## Prefix/Game Setup

1. Open Steam.
2. Add the NIKKE installer as a non-Steam game.
3. Right-click the entry and open **Properties**.
4. Enable compatibility and select **DW Proton**.
5. Launch the installer once so Steam creates the prefix.
6. Let the installer download and install NIKKE.
7. Find the prefix under Steam's `compatdata` directory. Non-Steam games usually use a random numeric folder.

   Common prefix locations:

   ```text
   Native Steam: ~/.steam/root/steamapps/compatdata/
   Flatpak Steam: ~/.var/app/com.valvesoftware.Steam/data/Steam/steamapps/compatdata/
   Snap Steam: ~/snap/steam/common/.steam/steam/steamapps/compatdata/
   Other Steam library: <library-path>/steamapps/compatdata/
   ```

   Sort by latest modified time after launching the installer to identify the new non-Steam prefix.

8. Change the non-Steam game's executable path to:

   ```text
   <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
   ```

9. Disable Steam Overlay for this non-Steam game.

## Install/Update Notes

This path intentionally excludes Windows. The Gist states that Steam itself is not the discouraged path; only the old Windows + Steam transfer path is last resort.

Updates should be handled through the launcher when using DW Proton.

Shared troubleshooting lives in [known issues](../../known-issues.md).

<br />

## Preview

https://github.com/user-attachments/assets/e277b735-c9cf-4068-9e8d-fa6d6b019f4c

_I can't help with the compression, anything bigger than 10MB = no preview_

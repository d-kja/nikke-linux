# Steam: miniloader

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Steam for Linux
- [wine-miniloader](https://dawn.wine/NelloKudo/wine-miniloader/releases)

## Runner Setup

Steam only lists runners that are installed as Steam compatibility tools. The folder under `compatibilitytools.d` needs the Steam compatibility-tool metadata, not just a bare Wine directory.

1. Download the miniloader release from [Dawn Winery](https://dawn.wine/NelloKudo/wine-miniloader/releases).
2. Create Steam's custom compatibility tool directory if it does not exist:

   ```text
   Native Steam: ~/.steam/root/compatibilitytools.d/
   Flatpak Steam: ~/.var/app/com.valvesoftware.Steam/data/Steam/compatibilitytools.d/
   Snap Steam: ~/snap/steam/common/.steam/steam/compatibilitytools.d/
   ```

   On many native installs, `~/.steam/root/` and `~/.steam/steam/` point at the same Steam directory. Prefer `~/.steam/root/compatibilitytools.d/` unless your distro documents a different Steam root.

3. Extract the miniloader runner into the matching `compatibilitytools.d` directory. Do not flatten the archive; Steam expects one runner folder under `compatibilitytools.d`.

   Example native layout:

   ```text
   ~/.steam/root/compatibilitytools.d/miniloader-<version>/
   ```

4. Check that the runner folder contains Steam compatibility tool files such as `compatibilitytool.vdf`, `proton`, and `toolmanifest.vdf`.

   If the package only contains Wine files such as `bin/wine`, `bin/wineserver`, and `lib/wine/`, Steam will not show it as a Proton runner by itself. Use a Proton-formatted miniloader package or wrapper for Steam, or use that Wine runner through Bottles, Heroic, or Faugus instead.

5. Restart Steam.
6. Confirm miniloader appears under the non-Steam game's compatibility options.

## Prefix/Game Setup

1. Open Steam.
2. Add the NIKKE installer as a non-Steam game.
3. Right-click the entry and open **Properties**.
4. Enable compatibility and select the miniloader runner if available.
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

Updates should be handled through the launcher if the runner works correctly. Shared update caveats live in [known issues](../../known-issues.md).

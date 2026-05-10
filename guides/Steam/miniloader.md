# Steam: miniloader

## Verification Status

Inferred and needs testing.

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Steam for Linux
- [wine-miniloader](https://dawn.wine/NelloKudo/wine-miniloader/releases)

## Runner Setup

This path is inferred from the Bottles miniloader path and the Gist's note that Steam can work with custom runners. It needs testing.

1. Install miniloader where Steam can use it as a compatibility tool.
2. Restart Steam.
3. Confirm miniloader appears under the non-Steam game's compatibility options.

## Prefix/Game Setup

1. Open Steam.
2. Add the NIKKE installer as a non-Steam game.
3. Right-click the entry and open **Properties**.
4. Enable compatibility and select the miniloader runner if available.
5. Launch the installer once so Steam creates the prefix.
6. Let the installer download and install NIKKE.
7. Find the prefix under Steam's `compatdata` directory. Non-Steam games usually use a random numeric folder.
8. Change the non-Steam game's executable path to:

   ```text
   <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
   ```

9. Disable Steam Overlay for this non-Steam game.

## Install/Update Notes

Updates should be handled through the launcher if the runner works correctly. Shared update caveats live in [known issues](../../known-issues.md).

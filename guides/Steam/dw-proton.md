# Steam: DW Proton

## Verification Status

Inferred from the Gist's Steam note and current recommendation that Steam can use DW Proton without Windows.

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Steam for Linux
- [DWPROTON](https://dawn.wine/dawn-winery/dwproton)

## Runner Setup

1. Install DW Proton where Steam can use it as a compatibility tool.
2. Restart Steam after installing DW Proton.
3. Confirm DW Proton appears under the non-Steam game's compatibility options.

## Prefix/Game Setup

1. Open Steam.
2. Add the NIKKE installer as a non-Steam game.
3. Right-click the entry and open **Properties**.
4. Enable compatibility and select **DW Proton**.
5. Launch the installer once so Steam creates the prefix.
6. Let the installer download and install NIKKE.
7. Find the prefix under Steam's `compatdata` directory. Non-Steam games usually use a random numeric folder.
8. Change the non-Steam game's executable path to:

   ```text
   <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
   ```

9. Disable Steam Overlay for this non-Steam game.

## Install/Update Notes

This path intentionally excludes Windows. The Gist states that Steam itself is not the discouraged path; only the old Windows + Steam transfer path is last resort.

Updates should be handled through the launcher when using DW Proton.

Shared troubleshooting lives in [known issues](../../known-issues.md).

# Last Resort: Windows + Steam

## Verification Status

Confirmed from the Gist, but marked as last resort.

## Requirements

- A Linux distribution
- Access to a Windows machine
- Steam for Linux
- [DWPROTON](https://dawn.wine/dawn-winery/dwproton) or [Proton GE](https://github.com/GloriousEggroll/proton-ge-custom)
- A USB drive or another way to transfer files

## Runner Setup

1. Install Steam on Linux.
2. Install DW Proton or Proton GE where Steam can use it as a compatibility tool.
3. Restart Steam after installing the runner.

## Prefix/Game Setup

1. On Windows, download the NIKKE installer from the [official website](https://nikke-en.com).
2. Install and download the full game.
3. Copy the entire `NIKKE` folder to a USB drive or transfer it to your Linux machine.
4. On Linux, download the launcher from the official website.
5. Add the launcher as a non-Steam game.
6. Run it once through Steam so Steam creates a prefix.
7. Find the prefix under:

   ```text
   ~/.steam/steam/steamapps/compatdata/
   ```

   Non-Steam games usually have a random 10-digit folder name. Sort by latest modified time to find the right folder.

8. Copy the Windows `NIKKE` folder into the prefix's `drive_c` directory.
9. Right-click the game in Steam and open **Properties**.
10. Set the compatibility layer to **Proton GE** or **DWPROTON**.

## Install/Update Notes

1. In Steam **Properties**, update the executable path to:

   ```text
   <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
   ```

2. Disable Steam Overlay.
3. Launch through Steam.
4. Log in and start the game.

When the game updates, you may need to re-download the updated game on Windows and repeat the transfer. This is why this path is a last resort.

Shared troubleshooting lives in [known issues](../../known-issues.md).

# Faugus: miniloader

## Verification Status

Inferred and needs testing.

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Faugus Launcher, installed via Flatpak or your package manager
- [wine-miniloader](https://dawn.wine/NelloKudo/wine-miniloader/releases)

## Runner Setup

This path is inferred from the Bottles miniloader path and the Faugus DW Proton path. It needs testing in Faugus.

1. Download the miniloader release from [Dawn Winery](https://dawn.wine/NelloKudo/wine-miniloader/releases).
2. Extract the archive.
3. Place the extracted runner where Faugus can detect custom Wine/Proton runners.
4. Restart Faugus and check whether the miniloader runner appears in the runner list.

## Prefix/Game Setup

1. Open Faugus.
2. Click `+`.
3. Set **Type** to **Windows Game**.
4. Set **Name** to `Goddess of Victory NIKKE`.
5. Choose a prefix location.
6. Leave **PATH** blank until after installation.
7. Select the miniloader runner if it appears.

## Install/Update Notes

1. Go to **Tools -> Winetricks**.
2. Select the default wineprefix.
3. Install required fonts:
   - `arial`, or
   - `allfonts`
4. Optionally install:
   - `mfc42`
   - `vcredist2012` or `vcrun2012`
   - `vcredist2022` or `vcrun2022`
5. Close Winetricks.
6. Go to the **Tools** tab.
7. Click **RUN**.
8. Select the NIKKE installer `.exe`.
9. Wait for the download and install to finish.
10. Return to the **Game/App** tab.
11. Set **PATH** to:

    ```text
    <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
    ```

12. Launch through Faugus.

Updates should be handled through the launcher if the runner works correctly. Shared update caveats live in [known issues](../../known-issues.md).

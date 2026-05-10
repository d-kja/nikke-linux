# Faugus: DW Proton

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Faugus Launcher, installed via Flatpak or your package manager
- DW-Proton Latest, installed through ProtonPlus, another third-party installer, or manually

## Runner Setup

### Option 1: ProtonPlus Or Another Third-Party Installer

1. Install ProtonPlus or another runner installer that supports Faugus.
2. Open the installer.
3. Install **DW-Proton Latest**.
4. Close the installer.

Faugus should auto-detect DW-Proton after installation.

### Option 2: Manual Download

1. Download DW Proton from [Dawn Winery](https://dawn.wine/dawn-winery/dwproton). Select the latest release archive.
2. Extract the archive.
3. Place the extracted runner where Faugus can detect custom Wine/Proton runners.
4. Restart Faugus.
5. Confirm DW-Proton appears in Faugus's Proton runner selection.

## Prefix/Game Setup

1. Open Faugus.
2. Click `+`.
3. Set **Type** to **Windows Game**.
4. Set **Name** to `Goddess of Victory NIKKE`.
5. For **Prefix**, click the search button and choose the prefix location, such as a game drive.
6. Leave **PATH** blank for now.
7. Set **Proton** to **DW-Proton Latest**.
8. Enable shortcuts if you want them.

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

12. Enable shortcuts if needed and click **OK**.
13. Launch through Faugus with DW-Proton.

Updates should be handled through the launcher.

Shared troubleshooting lives in [known issues](../../known-issues.md).

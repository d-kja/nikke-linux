# Faugus: DW Proton

## Verification Status

User-tested and approved for inclusion from the supplied comment.

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Faugus Launcher, installed via Flatpak or your package manager
- [ProtonPlus](https://protonplus.vysp3r.com/#download)
- DW-Proton Latest, installed through ProtonPlus

## Runner Setup

1. Install ProtonPlus from [the ProtonPlus download page](https://protonplus.vysp3r.com/#download).
2. Open ProtonPlus.
3. Install **DW-Proton Latest**.
4. Close ProtonPlus.

Faugus should auto-detect DW-Proton after installation.

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

# Bottles: DW Proton

## Verification Status

Confirmed from the Gist.

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- [Bottles](https://usebottles.com), installed via Flatpak or native package
- [DWPROTON](https://dawn.wine/dawn-winery/dwproton)

## Runner Setup

1. Download DW Proton from [Dawn Winery](https://dawn.wine/dawn-winery/dwproton). Select the latest release archive.
2. Extract it:

   ```bash
   tar -xvf [DOWNLOADED_FILE].tar.xz
   ```

3. Move the extracted folder to the Bottles runners directory:
   - Flatpak: `~/.var/app/com.usebottles.bottles/data/bottles/runners/`
   - Native package: `~/.local/share/bottles/runners/`

## Prefix/Game Setup

1. Open Bottles.
2. Click **Create** in the top-right corner.
3. Select **Gaming** as the environment.
4. Select **dwproton** as the runner.

If `dwproton` does not appear as a runner option, the runner was not placed in the correct directory.

## Install/Update Notes

1. Open the bottle's **Dependencies** page.
2. Install required fonts:
   - `arial`, or
   - `allfonts` if you want the broader font bundle
3. Optionally install:
   - `mfc42`
   - `vcredist2012`
   - `vcredist2022`
4. Click **Run Executable** and select the NIKKE installer.
5. Wait for the game to finish downloading.
6. Click **Add Shortcuts** and select:

   ```text
   <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
   ```

7. Run the launcher from Bottles.

Updates should be handled through the launcher.

Shared troubleshooting lives in [known issues](../../known-issues.md).

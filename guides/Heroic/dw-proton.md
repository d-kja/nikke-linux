# Heroic: DW Proton

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Heroic Games Launcher
- [DWPROTON](https://dawn.wine/dawn-winery/dwproton)

## Runner Setup

This path is inferred from the Gist's note that other launchers supporting custom Wine runners can work. It needs Heroic-specific testing.

### Option 1: ProtonPlus Or Another Third-Party Installer

1. Install ProtonPlus or another runner installer that supports Heroic.
2. Select Heroic as the target launcher if the installer asks.
3. Install **DW-Proton Latest** or the latest DW Proton release.
4. Restart Heroic.
5. Confirm DW Proton appears in Heroic's Wine/Proton runner selection.

### Option 2: Manual Download

1. Install Heroic Games Launcher.
2. Install DW Proton where Heroic can detect custom Wine/Proton runners.
3. Restart Heroic.
4. Confirm DW Proton appears in Heroic's Wine/Proton runner selection.

## Prefix/Game Setup

1. Create a new non-store game entry in Heroic for NIKKE.
2. Select DW Proton as the runner.
3. Create or choose a Wine prefix for the game.
4. Run the NIKKE installer inside that prefix.
5. After installation, set the game executable to:

   ```text
   <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
   ```

## Install/Update Notes

Updates should be handled through the launcher if Heroic runs the prefix correctly with DW Proton.

Shared troubleshooting lives in [known issues](../../known-issues.md).

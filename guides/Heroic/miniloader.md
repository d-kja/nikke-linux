# Heroic: miniloader

## Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)
- Heroic Games Launcher
- [wine-miniloader](https://dawn.wine/NelloKudo/wine-miniloader/releases)

## Runner Setup

This path is inferred from the Bottles miniloader path and the Gist's note that other launchers supporting custom Wine runners can work. It needs Heroic-specific testing.

1. Install Heroic Games Launcher.
2. Install miniloader where Heroic can detect custom Wine/Proton runners.
3. Restart Heroic.
4. Confirm miniloader appears in Heroic's Wine/Proton runner selection.

## Prefix/Game Setup

1. Create a new non-store game entry in Heroic for NIKKE.
2. Select miniloader as the runner.
3. Create or choose a Wine prefix for the game.
4. Run the NIKKE installer inside that prefix.
5. After installation, set the game executable to:

   ```text
   <prefix-path>/drive_c/NIKKE/Launcher/nikke_launcher.exe
   ```

## Install/Update Notes

Updates should be handled through the launcher if Heroic runs the prefix correctly with miniloader. Shared update caveats live in [known issues](../../known-issues.md).

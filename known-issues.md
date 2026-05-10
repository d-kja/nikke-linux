# Known Issues and Caveats

## Startup Issues

- The launcher may require multiple start/cancel attempts before opening.
- Anti-cheat may complain occasionally; restarting usually fixes it.

## Account and Launcher State

- The launcher may not remember your password.
- The game may forget your server region.
- Use Steam login at your discretion. Nikke doesn't support this by default, and without DW Proton it's literally not working.

## Quitting the Game

- When quitting, you may need to stop the process from the launcher, Bottles, or Steam.

## Video Playback

- Video playback is a known issue on some setups. Try switching between launchers to see if it resolves on your end.
  - You can try downloading mf, mfplat, windowscodecs, quartz, and devenum
  - NVIDIA specific:
    - Downgrade your driver to test
    - You can try using `GST_PLUGIN_FEATURE_RANK=nvh264dec:0,nvdec:0,nvh265dec:0`
   
_Note: none of those solutions are guaranteed, but you can try using them._

## Updates

- DW Proton paths should update through the launcher when working correctly.
- Some updates might require moving the content from `update_files` into the parent directory.
- The Windows + Steam path will require re-downloading the updated game on Windows and transferring it again, which is why it is a last-resort path.

## Inferred Launcher Paths

- Heroic DW Proton, Heroic miniloader, and Steam miniloader need testing.

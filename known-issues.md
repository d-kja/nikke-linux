# Known Issues and Caveats

This file centralizes shared caveats for all NIKKE Linux paths. Launcher-specific guides should stay focused on setup steps and should not duplicate this section.

## Source Policy

- Gist-backed information is the source of truth for confirmed paths.
- The Faugus DW Proton path is included because a user-tested comment was explicitly approved for inclusion.
- Paths are labeled individually as confirmed, user-tested, inferred, or needing testing.
- Comment-only troubleshooting should not be promoted as confirmed unless it is explicitly approved later.

## Startup Issues

- The launcher may require multiple start/cancel attempts before opening.
- Anti-cheat may complain occasionally; restarting usually fixes it.

## Account and Launcher State

- The launcher may not remember your password.
- The game may forget your server region.

## Quitting the Game

- When quitting, you may need to stop the process from the launcher, Bottles, or Steam.

## Updates

- DW Proton paths should update through the launcher when working correctly.
- The Bottles miniloader path has a known update caveat from the Gist: some updates might require moving `update_files` into the launcher directory.
- The Windows + Steam path may require re-downloading the updated game on Windows and transferring it again, which is why it is a last-resort path.

## Inferred Launcher Paths

- Faugus miniloader, Heroic DW Proton, Heroic miniloader, and Steam miniloader need testing.
- If an inferred runner is not detected by the launcher, use a confirmed or stronger path such as Bottles + DW Proton, Bottles + miniloader, Lutris, Faugus + DW Proton, or Steam + DW Proton.

## Terms of Service Risk

- Do not document community patches or anti-cheat workarounds that may create Terms of Service risk unless the maintainer explicitly decides to include them with a warning.

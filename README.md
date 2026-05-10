# Running NIKKE on Linux

This repository expands the Linux guide for **GODDESS OF VICTORY: NIKKE** into launcher-specific paths.

The Gist remains the short path list. This repository contains the detailed guides linked from that list.

> [!IMPORTANT]
> Existing Gist-backed paths are treated as the source of truth. Gist comments are not used to rewrite confirmed paths unless a specific user-tested path is approved for inclusion.

## Paths

| Path | Best For | Status | Guide |
|---|---|---|---|
| Bottles + DW Proton | Recommended Bottles setup | Confirmed from the Gist | [Guide](guides/Bottles/dw-proton.md) |
| Bottles + miniloader | Bottles users who want the miniloader runner | Confirmed from the Gist | [Guide](guides/Bottles/miniloader.md) |
| Lutris script | Lutris users who want a script-based install | Confirmed from the Gist | [Guide](guides/Lutris/script.md) |
| Faugus + DW Proton | Faugus users who want DW Proton | User-tested and approved for inclusion | [Guide](guides/Faugus/dw-proton.md) |
| Faugus + miniloader | Faugus users testing the miniloader runner | Inferred, needs testing | [Guide](guides/Faugus/miniloader.md) |
| Heroic + DW Proton | Heroic users testing DW Proton | Inferred, needs testing | [Guide](guides/Heroic/dw-proton.md) |
| Heroic + miniloader | Heroic users testing miniloader | Inferred, needs testing | [Guide](guides/Heroic/miniloader.md) |
| Steam + DW Proton | Steam users who want to avoid Windows | Inferred from the Gist Steam note | [Guide](guides/Steam/dw-proton.md) |
| Steam + miniloader | Steam users testing miniloader | Inferred, needs testing | [Guide](guides/Steam/miniloader.md) |
| Windows + Steam | Last resort if Linux-side install paths fail | Confirmed from the Gist, but not recommended | [Guide](guides/Last%20resort/windows-steam.md) |

## Shared Requirements

- A Linux distribution
- The NIKKE Windows installer from the [official website](https://nikke-en.com)

Each path has additional launcher and runner requirements in its guide.

## Recommended Order

1. Try a Linux-only path first: Bottles + DW Proton, Bottles + miniloader, Lutris, Faugus + DW Proton, or Steam + DW Proton.
2. Try an inferred launcher path if you specifically use that launcher and are willing to test it.
3. Use Windows + Steam only as a last resort.

## Troubleshooting

Shared caveats and known issues are kept at the repository root: [known issues](known-issues.md).

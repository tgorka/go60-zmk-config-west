# Go60 firmware images

The built images kept for dockyard's Go60 device session (dockyard Epic 7, DR-32/DR-37).
Nothing here has been flashed yet. Verify against `SHA256SUMS` before you use a file.

| Folder | What | Built by | Halves |
| --- | --- | --- | --- |
| `studio-west-44817203815/` | ZMK Studio build prepared by dockyard: MoErgo default keymap, `&studio_unlock` on Magic + RH C2R2, 2 reserved layers, `studio-rpc-usb-uart` snippet and `CONFIG_USB_NRFX_EVT_QUEUE_SIZE=64` on the left half | GitHub Actions run 44817203815 of this repository, commit `3161743` plus zmk's `build-user-config.yml` pinned to `8266433d6b` | `go60_lh-zmk.uf2` (family `0x9809B007`, 1064 blocks), `go60_rh-zmk.uf2` (family `0x980AB007`, 747 blocks) |
| `stock-nix-44815164983/` | MoErgo's stock firmware, no Studio: the way back | GitHub Actions run 44815164983 of `tgorka/go60-zmk-config` (MoErgo's Nix template, untouched) | `go60.uf2`, both halves combined (943 LH + 743 RH blocks) |

Both builds track `moergo-sc/zmk` `main` on 2026-11-20, not the v26.09 tag.

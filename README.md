 # corne-zmk

  ZMK firmware config for a wireless Corne (crkbd) split keyboard using nice!nano v2 controllers with nice!view e-paper displays.

  ## Hardware

  - **Keyboard**: Corne (crkbd) — 42-key split
  - **Controllers**: nice!nano v2 (both halves)
  - **Displays**: nice!epaper via nice_view_adapter

  ## Layers

  | # | Label | Description |
  |---|-------|-------------|
  | 0 | `alpha` | QWERTY base with homerow mods |
  | 1 | `num` | Symbols and numpad |
  | 2 | `nav` | Mouse movement, scrolling, and arrow keys |
  | 3 | `bt` | Bluetooth selection, media, and brightness |
  | 4 | `game` | Gaming layout (no homerow mods) |

  ## Notable Features

  - **Homerow mods** — hold `A/S/D/F` and `J/K/L/;` for Alt/Ctrl/Shift/Cmd
  - **Mouse control** — cursor movement, clicks (L/R/MB4/MB5), and scroll on the nav layer
  - **ZMK Studio** — runtime keymap editing without reflashing ([zmk.studio](https://zmk.studio))
  - **Sleep** — idle timeout at 60s to preserve battery
  - **Bluetooth TX power** — boosted to +8 dBm

  ## Building

  Firmware is built via GitHub Actions on push. The workflow produces `.uf2` files for both halves.

  To flash manually:
  1. Download the artifacts from the latest Actions run
  2. Put the controller in bootloader mode (double-tap reset)
  3. Copy the `.uf2` to the mounted drive

  ## Config

  - `config/corne.keymap` — keymap and layer definitions
  - `config/corne.conf` — Kconfig options (display, BT, sleep, ZMK Studio)
  - `build.yaml` — shield/board targets for the CI build


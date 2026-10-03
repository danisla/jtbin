# Game Bub cores

Arcade cores for the [Game Bub](https://gamebub.net/) handheld, built from
[jtcores](https://github.com/jotego/jtcores) with a Game Bub JTFRAME target
(the gamebub-jtcores project).

* `raw/cores/<ID>/`: the core definition and bitstream, as they appear on the SD card.
* `zips/<id>.zip`: the same content ready to unzip at the root of the SD card.

Each core supports a single main MAME set. ROMs are not included: generate the
`.rom` file with the same MRA/`mra` tool flow as MiSTer, or with
`scripts/make_rom.py` from gamebub-jtcores, and copy it to `roms/arcade/`.

| Core | Game | ROM file |
|------|------|----------|
| JT1942 | 1942 | `1942.rom` |
| JT1943 | 1943: The Battle of Midway | `1943.rom` |
| JTDD | Double Dragon (World set 1) | `ddragon.rom` |
| JTDD2 | Double Dragon II: The Revenge | `ddragon2.rom` |
| JTGNG | Ghosts'n Goblins (World?) | `gng.rom` |
| JTCONTRA | Contra (US - Asia, set 1) | `contra.rom` |

Double Dragon II's priority PROM (`21j-k-0`) is in `ddragon.zip`, not
`ddragon2.zip`: `make_rom.py` merges it in (`extra_zips` in `cores.json`). A
`.rom` made without it shows only the text layer, with black gameplay.

The cores are covered by the same license as the rest of this repository: use
them only with ROM files you legally own.

# cod2-configs

Player setups for Call of Duty 2, collected from public pages and credited to where they were
published. [CoD2 Silicon](https://github.com/cod2unbound/cod2-unbound) shows them under
Configs · Home, where a setup is reviewed line by line before anything is imported.

The list of setups is in [INDEX.md](INDEX.md).

## What is in an entry

Each folder under `entries/` holds two files.

- `config.cfg` is the text its source published, with lines left out. It keeps settings and key
  binds of the game. It leaves out the player's name, chat lines, passwords and logins, file paths
  and hardware details, server addresses, settings for hosting a server, timed key macros, and
  settings that belong to other games. The lines that remain keep their order and their bytes.
- `entry.json` says who the setup is credited to, the page it came from (`sourceURL`), the day the
  copy was taken, and how the name got on it: `self-published` (the player posted it), `listed` (a
  page lists it under that name) or `uploaded` (someone uploaded it under that name). It also says
  how many lines were left out and why.

The catalogue does not claim that a player approved a listing, and `listed` and `uploaded` entries
are not proof of who made a config. Sensitivity values cannot be compared between players without
the mouse's DPI, which no published config gives.

## Ask for a removal or a correction

If a setup here is yours, or is credited to the wrong person, open an issue:
<https://github.com/cod2unbound/cod2-configs/issues/new>. Say which entry and what should change. It
will be removed or corrected, no reason needed.

## How the catalogue is built

The tools are in the CoD2 Silicon repository under
[`tools/config-directory`](https://github.com/cod2unbound/cod2-unbound/tree/main/tools/config-directory).
`clean` prepares a published config with the launcher's own import review, `generate.py` checks
every entry and writes `index.json`, and the maintainer signs the index. The launcher only accepts
an index whose signature (`index.sig`) matches the public key it was built with (`index.pub`), and
only a config whose checksum matches its entry.

`review.json` records, for each entry and each game version, how many lines the launcher's review
calls safe and how many it asks about before importing.

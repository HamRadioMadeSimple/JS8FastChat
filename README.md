# JS8FastChat

A compact chat window for working one JS8Call station, with an inbox, watch words and one-click queries. Companion app to **[JS8Map Spotter](https://github.com/HamRadioMadeSimple/JS8MapSpotter)**: one click on a station on the map opens it here.

**JS8FastChat 1.76 — Windows and Linux**

**[Download the latest release](../../releases/latest)** · [Guides (PDF)](docs) · [Video](https://youtu.be/yx9uM26-_6w) · [Website](https://hamradiomadesimple.github.io/)

## Videos

- [JS8FastChat - Companion App to JS8Map Spotter](https://youtu.be/yx9uM26-_6w)
- [Overview of the JS8FastChat App](https://youtu.be/yJJw8RieM4U)

## What it does

Work a selected station without going back to the JS8Call interface.

- Full JS8Call control for that station: send, directed messages, HALT
- Signal report, distance and one-click queries (SNR, INFO, GRID, STATUS, HEARING)
- Message store and inbox
- Watch words
- Follows other traffic on frequency
- Runs on its own, or opens from JS8Map Spotter with one click

## Related

**[JS8Map Spotter](https://github.com/HamRadioMadeSimple/JS8MapSpotter)** — every station JS8Call hears on a live, offline map, with CommStat StatReps, MCForms and QSOs between other stations. It replaces JS8Map 1.75 and opens stations in JS8FastChat.

**[FCC Lookup](https://github.com/HamRadioMadeSimple/FCC_Lookup)** — offline callsign lookup for U.S. FCC and Canadian amateur licenses.

## Requirements

- **JS8Call**, running, with its TCP API enabled
- **TCP Max Connections set to 5** in JS8Call
- Windows 10 or later, or a current Linux desktop

JS8FastChat talks to JS8Call over its network API. It does not modify JS8Call.

## Installing

Installers for Windows and packages for Linux are on the [Releases](../../releases) page. Illustrated JS8FastChat guides are in the [docs](docs) folder.

**JS8FastChat on Linux:** download the `_Linux.tar.gz` into Downloads and paste the three lines in [the JS8FastChat README](JS8FastChat%20Ver%201.76/README.md#install-on-linux), or follow [Installing JS8FastChat on Linux](docs/Installing_JS8FastChat_on_Linux.pdf).

## Building from source

JS8FastChat is Python. The Windows build uses PyInstaller driven by `Build_JS8FastChat.bat`, with Inno Setup for the installer. The Linux package is its Python source, run with the system's Python and Tk, so nothing is compiled; `tools/make_release.py` in its folder builds every package. How FastChat is put together is in its [ARCHITECTURE.md](JS8FastChat%20Ver%201.76/ARCHITECTURE.md).

`shared_resolver.py` must stay byte-identical with the copy in JS8Map Spotter and in `JS8Map Ver 1.75`; `check_twins.bat` checks the local pair before a Windows build.

**`JS8Map Ver 1.75`** is the older map program that used to ship with JS8FastChat (and its releases up to 1.75.1). It has been replaced by [JS8Map Spotter](https://github.com/HamRadioMadeSimple/JS8MapSpotter) and is kept here only for reference and for the build check.

Callsign databases are not included. They are built on first run from public license data.

## Credits

**JS8Call** by KN4CRD and contributors. JS8FastChat is an independent companion and is not affiliated with or endorsed by the JS8Call project.

**Leaflet** — map display library, © Vladimir Agafonkin and contributors, BSD 2-Clause licensed.

**Map data** — © OpenStreetMap contributors, available under the Open Database License. Basemap styling © CARTO.

**FCC license database** — United States government work, public domain. **Canadian amateur callsign data** — open data published by ISED Canada.

## License

Copyright (C) 2026 MJ Jordan (KW3KW)

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

The full license text is in [LICENSE](LICENSE).

## Reporting problems

Open an issue on the [Issues](../../issues) tab. Please include: Windows or Linux, your JS8Call version, and what you expected to happen.

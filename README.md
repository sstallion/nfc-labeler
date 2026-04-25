# 3D Filament Labels

[![](https://github.com/sstallion/nfc-labeler/actions/workflows/ci.yml/badge.svg?branch=main)][1]
[![](https://img.shields.io/github/v/release/sstallion/nfc-labeler)][2]
[![](https://img.shields.io/github/license/sstallion/nfc-labeler.svg)][3]

This repository contains a command-line utility that generates 3D printer
filament labels for [Santek EZ Sign][4] displays with a similar look and feel to
those created by the [3D Filament Profile Database][5]. Community [assets][6]
and [file formats][7] are reused where possible and are the work of their
respective authors.

## Supported Hardware

- [Santek EZ Sign][4] 2.9" 2- &amp; 4-color displays
- [Sony RC-S300/S1][8] USB NFC reader/writer

## Getting Started

> [!IMPORTANT]
> This guide assumes you have a functioning Python 3.12 (or later) environment
> with [uv][10] installed and available in `$PATH`. On Linux, [pcsclite][11]
> must also be installed as a [dependency][12].

Due to the experimental nature of this project, packages are not published to
[PyPI][9] and must be installed locally.

The main script can be called by issuing:

```shell
uv run nfc-labeler [OPTIONS] COMMAND [ARGS]...
```

Python wheels are also available for download from the [Releases][13] page.

### Usage

```
Usage: nfc-labeler [OPTIONS] COMMAND [ARGS]...

  Generates 3D printer filament labels for Santek EZ Sign displays

Options:
  --help  Show this message and exit.
```

## Contributing

Pull requests are welcome! See [Contributing][14] for details.

## License

Source code in this repository is licensed under a Simplified BSD License. See
[LICENSE][3] for details.

[1]: https://github.com/sstallion/nfc-labeler/actions/workflows/ci.yml
[2]: https://github.com/sstallion/nfc-labeler/releases/latest
[3]: https://github.com/sstallion/nfc-labeler/blob/main/LICENSE
[4]: https://santekdisplay.com/en
[5]: https://3dfilamentprofiles.com/
[6]: https://github.com/MarksMakerSpace/filament-profiles
[7]: https://3dfilamentprofiles.com/help#data-export
[8]: https://www.sony.co.jp/en/Products/felica/business/products/RC-S300S1.html
[9]: https://pypi.org/
[10]: https://docs.astral.sh/uv/getting-started/installation/
[11]: https://pcsclite.apdu.fr/
[12]: https://pyscard.sourceforge.io/user-guide.html#introduction
[13]: https://github.com/sstallion/nfc-labeler/releases
[14]: https://github.com/sstallion/nfc-labeler/blob/main/CONTRIBUTING.md

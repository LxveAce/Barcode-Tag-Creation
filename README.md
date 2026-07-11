# Barcode Label Generator

A Windows desktop app for making measurement-accurate, vector PDF labels with Code 128B barcodes. Point it at a spreadsheet and get one scannable label per page, sized to the exact inch.

[![Release](https://img.shields.io/github/v/release/LxveAce/Barcode-Tag-Creation?label=release&color=2b6cb0)](https://github.com/LxveAce/Barcode-Tag-Creation/releases/latest)
[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://www.python.org/)
![GUI](https://img.shields.io/badge/GUI-CustomTkinter-2b6cb0)
![PDF](https://img.shields.io/badge/PDF-ReportLab-444)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?logo=windows&logoColor=white)
[![License](https://img.shields.io/github/license/LxveAce/Barcode-Tag-Creation?color=green)](LICENSE)

Each label pairs a text caption with a Code 128B barcode, and the label data comes straight from Excel or CSV. Everything is placed relative to the center of the page in inch offsets, so a label measures out exactly as designed when you print at 100%.

This is the predecessor to Tag Studio — a single-purpose label generator rather than the full label suite. For the bigger toolkit, see [ExpertTags](https://experttags.com).

## Features

- **Vector PDF output** — text and bars render as true vectors (ReportLab), so they stay crisp at any print size.
- **Code 128B barcodes** — one barcode plus a text caption per label.
- **Excel or CSV input** — drive a whole batch from a two-column spreadsheet.
- **Center-anchored layout** — every element is positioned relative to the page center in inch offsets, so labels measure out exactly as designed.
- **Configurable page size** — set the page dimensions (for example 11 x 4 inches) before exporting.

## Download

Grab `BarcodeLabeler.exe` from the [latest release](https://github.com/LxveAce/Barcode-Tag-Creation/releases/latest) and run it on Windows — no Python install required.

The binary is unsigned, so Windows SmartScreen may warn on first run ("More info" → "Run anyway").

Verify the download before running it. The SHA-256 of `BarcodeLabeler.exe` for **v1.0.0** is:

`0080a2e6616d8591bc45ce04236fb0173357412a21a8f0440611dc21ce7aa345`

Compute the hash on Windows and confirm it matches:

```powershell
Get-FileHash BarcodeLabeler.exe -Algorithm SHA256
```

## CSV format

```csv
item_name,barcode_value
Widget A,WIDGETA-001
Widget B,WIDGETB-002
```

Each row makes one label: `item_name` becomes the caption and `barcode_value` is encoded as the Code 128B barcode. Excel workbooks use the same two-column shape.

Code 128B only encodes ASCII characters 32–127, so keep `barcode_value` within that range.

## Layout

- All offsets are relative to the **center of the page**.
- `0` = centered. Negative X = left, positive X = right. Negative Y = down, positive Y = up.
- Set the page dimensions before exporting.
- Print at **Actual size / 100%** (no scaling) for accurate measurements.

More build notes on symbology, coordinates, and verification are in [docs/LABEL-TAG-ENGINEERING.md](docs/LABEL-TAG-ENGINEERING.md).

## Security

Please report security issues privately — see [SECURITY.md](SECURITY.md). Don't open a public issue for a vulnerability.

## License

Released under the [MIT License](LICENSE). Provided **as-is**, with no warranty. Always verify generated labels and barcodes against your label stock, printer, and scanner before any production use.

## Connect

**Discord:** [discord.gg/lxvelabs](https://discord.gg/lxvelabs) · **GitHub:** [@LxveAce](https://github.com/LxveAce) · **Email:** LxveLabs@proton.me (business) · lxveace@proton.me (direct) · **Site:** [experttags.com](https://experttags.com)

Part of the ExpertTags label toolkit · built by LxveAce

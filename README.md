# Barcode Tag Creation

A Windows desktop app for generating **measurement-accurate, vector** PDF labels with **Code 128B** barcodes. Built with Python and CustomTkinter, it pairs a text caption with a scannable barcode on each label and pulls label data straight from **Excel** or **CSV**.

This is the predecessor to Tag Studio — a focused, single-purpose label generator rather than a full label suite.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![CustomTkinter](https://img.shields.io/badge/GUI-CustomTkinter-2b6cb0)
![Barcode](https://img.shields.io/badge/Barcode-Code%20128B-444)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?logo=windows&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

## Features

- **Vector PDF output** — labels render as true vectors, so text and bars stay crisp at any print size.
- **Code 128B barcodes** — one barcode plus a text caption per label/page.
- **Excel or CSV input** — drive a batch of labels from a spreadsheet.
- **Center-anchored layout** — every element is positioned relative to the page center using inch offsets, so labels measure out exactly as designed.
- **Configurable page size** — set the page dimensions (for example, 11 x 4 inches) before exporting.

## Download

The latest packaged build is published on the [Releases page](https://github.com/LxveAce/Barcode-Tag-Creation/releases). Download `BarcodeLabeler.exe` from the latest release and run it directly on Windows — no Python install required.

## CSV Format

```csv
item_name,barcode_value
Widget A,WIDGETA-001
Widget B,WIDGETB-002
```

Each row produces one label: `item_name` becomes the caption and `barcode_value` is encoded as the Code 128B barcode. Excel workbooks follow the same two-column shape.

## Layout

- All offsets are relative to the **center of the page**.
- `0` = centered. Negative X = left, positive X = right. Negative Y = down, positive Y = up.
- Set the page dimensions before exporting.
- Print at **Actual size / 100%** (no scaling) for accurate measurements.

## Security

To report a security issue, see [SECURITY.md](../SECURITY.md). Please do not open a public issue for vulnerabilities.

## License

Released under the [MIT License](../LICENSE). Provided **as-is**, with no warranty. Always verify generated labels and barcodes against your label stock, printer, and scanner before any production use.

## Connect

- **Discord:** [discord.gg/lxveace](https://discord.gg/lxveace) — questions, help, or to talk through this project
- **GitHub:** [@LxveAce](https://github.com/LxveAce)
- **Website:** [lxveace.com](https://lxveace.com)
- **Project site:** [experttags.com](https://experttags.com)

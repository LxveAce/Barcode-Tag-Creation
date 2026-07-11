# Barcode Label Generator — usage reference

A Windows desktop app that generates measurement-accurate, vector PDF labels:

- Text caption + Code 128B barcode per page
- Data sourced from **Excel** or **CSV**
- All positioning is center-anchored with inch offsets

This repo ships the packaged app; the app source isn't published here. See the top-level [README](../README.md) for the full overview.

## Run

Download `BarcodeLabeler.exe` from the [latest release](https://github.com/LxveAce/Barcode-Tag-Creation/releases/latest) and run it on Windows — no Python install required. Verify the SHA-256 first (checksum in the top-level README).

## CSV format

```csv
item_name,barcode_value
Widget A,WIDGETA-001
Widget B,WIDGETB-002
```

Excel workbooks (`.xlsx`) work the same way — use the same two columns as the CSV example. Code 128B only encodes ASCII 32–127, so keep `barcode_value` within that range.

## Layout

- All offsets are relative to the **center of the page**
- `0` = centered. Negative X = left, positive X = right. Negative Y = down, positive Y = up.
- Set page dimensions (e.g. 11 x 4) before exporting
- Print at **Actual size / 100%** (no scaling) for accurate measurements

## More

- [LABEL-TAG-ENGINEERING.md](LABEL-TAG-ENGINEERING.md) — general, reusable notes on symbology, coordinates, fonts, and verification.

## Disclaimer

Provided **as-is** under the MIT license, with no warranty. Always verify generated labels and barcodes against your label stock, printer, and scanner before any production use.

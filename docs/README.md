# Barcode Labeler (Code 128B) - Vector PDF

Python GUI to generate **measurement-accurate, vector** PDF labels:
- Text + Code 128B barcode per page
- Data sourced from **Excel** or **CSV**
- All positioning is center-anchored with inch offsets

## Setup

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

## Run

```bash
python app.py
```

Or double-click `run_gui.bat`.

## Download

Prefer a prebuilt binary? The latest packaged build is on the [Releases page](https://github.com/LxveAce/Barcode-Tag-Creation/releases) — download `BarcodeLabeler.exe` from the latest release and run it directly on Windows, no Python install required.

## CSV Format

```csv
item_name,barcode_value
Widget A,WIDGETA-001
Widget B,WIDGETB-002
```

Excel workbooks (`.xlsx`) work the same way — use the same two columns as the CSV example.

## Layout

- All offsets are relative to the **center of the page**
- `0` = centered. Negative X = left, positive X = right. Negative Y = down, positive Y = up.
- Set page dimensions (e.g. 11 x 4) before exporting
- Print at **Actual size / 100%** (no scaling) for accurate measurements

## Disclaimer

Provided **as-is** under the MIT license, with no warranty. Always verify generated labels and barcodes against your label stock, printer, and scanner before any production use.

# Python QR Generator

Small command-line helper that turns a URL (or any text) into an image-based QR code using the [`qrcode`](https://pypi.org/project/qrcode/) Python library.

## Prerequisites
- Python 3.8 or newer
- `pip` for installing dependencies

## Installation
```bash
python -m venv .venv
.venv\Scripts\activate  # On macOS/Linux use: source .venv/bin/activate
pip install qrcode[pil]
```

## Usage
```bash
python generator.py
```
You'll be prompted for:
- `URL`: Any text or link that should be encoded
- `filename`: The output image name (saved as `<filename>.jpg`)

Example:
```
Enter your URL: https://example.com
Enter the filename: example-qr
QR-Code generated!
```

The QR image is saved alongside the script, e.g. `example-qr.jpg`.

## Customizing
- Adjust the QR appearance (size, colors, error correction) by tweaking the arguments passed to `qrcode.QRCode` in `generator.py`.
- Replace `.jpg` with `.png` in the final `generate` call if you prefer PNG output.

## Troubleshooting
- **ModuleNotFoundError: No module named 'qrcode'**  
  Ensure the virtual environment is activated and rerun `pip install qrcode[pil]`.

Enjoy creating quick QR codes for links, Wi-Fi credentials, and more!

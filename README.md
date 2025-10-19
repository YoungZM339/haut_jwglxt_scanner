# haut_jwglxt_scanner

A lightweight asynchronous scanner that checks the HAUT JWGLXT network segment for reachable portal instances.

## Installation

```bash
pip install haut_jwglxt_scanner
```

## Usage

Run the bundled command-line interface:

```bash
haut_jwglxt_scan
```

Or integrate the scanner into your own script:

```python
from haut_jwglxt_scanner import JwglxtScanner
import asyncio

async def main():
    scanner = JwglxtScanner()
    await scanner.scan()
    scanner.save_results("jwglxt_urls.json")

asyncio.run(main())
```

The scan writes any discovered portals to `jwglxt_urls.json` by default.

## Development

This project uses Hatch for builds. To produce a wheel and source distribution:

```bash
hatch build
```

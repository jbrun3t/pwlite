# pwlite

See `README.md` for what the library does.

## Environment

Build your own venv if there is not already one.

```sh
python3 -m venv .venv
.venv/bin/pip install -e '.[dev]'
```

Run both before calling anything done, and have them clean:

```sh
.venv/bin/ruff check .
.venv/bin/ruff format .
```

## Patchwork

Do not hammer patchwork with requests. When trying things, read a few documents
or a page of a list, with a small `per_page`, rather than walking a whole
project.

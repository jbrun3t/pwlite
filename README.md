# pwlite

A small client for the [Patchwork](https://patchwork.readthedocs.io/) REST API
(1.3, patchwork 3.1 or later), one project of an instance at a time.

```python
from pwlite import Client

client = Client("https://patchwork.kernel.org", "linux-clk")
for patch in client.patches(state="new"):
    print(patch["id"], patch["name"])
```

- `patches()`, `events()`, `users()`: patchwork's filters as keyword arguments,
  paging through the results
- `project()`: the project, failing when patchwork does not know it
- `patch(id=…)`: one patch, refused if it belongs to another project
- `update_patch(id=…, **fields)`: writes the fields, with a token; nothing with
  `dry_run=True`
- errors raise `PwError`

## Install

```
python3 -m venv .venv
.venv/bin/pip install -e .
```

## License

MIT, see `LICENSE`.

# emoticond-data

The data files for [emoticond](https://github.com/Cloveian/emoticond): one
`.kmj` file per set, every version kept. Download a file; there is no need
to clone this repository.

```sh
emoticond data fetch                 # the latest core set into ~/.local/share/emoticond/
emoticond data fetch --set full      # or full / lite, or a version: emoticond data fetch 1.0
```

or by hand:

```sh
mkdir -p ~/.local/share/emoticond
curl -L -o ~/.local/share/emoticond/core.kmj https://raw.githubusercontent.com/Cloveian/emoticond-data/main/1/core.kmj
```

| set | |
|---|---|
| `core` | the default: every face that can reach a first page |
| `full` | every face |
| `lite` | `core` with shorter neighbour lists, for small devices |

Versions are `X.Y`: emoticond `X.*.*` reads data `X.*`, and emoticond
`X.Y.*` was made for data `X.Y`. The folder `X/` always holds the newest
`X.*`; each version also has its own folder. `SHA256SUMS` is in every
folder, and `versions.json` lists them all.

## Versions

| version | date | core | full | lite |
|---|---|---|---|---|
| `1.0` | 2026-10-07 | 69,668 faces, 12.8 MB | 176,126 faces, 24.3 MB | 69,668 faces, 11.1 MB |

## Licence

CC BY 4.0. The faces come from public kaomoji lists; the attributions are
inside each file (`emoticond info`) and in emoticond's docs/public-data.md.

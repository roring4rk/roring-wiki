# roring-wiki

Source for the Roring server wiki — **differences from vanilla pre-renewal RO only**.

Built with [mdBook](https://rust-lang.github.io/mdBook/). Deployed to GitHub Pages by
`.github/workflows/pages.yml`.

## Build locally

```sh
nix run nixpkgs#mdbook -- build       # output in book/
nix run nixpkgs#mdbook -- serve       # live preview on :3000
```

## Keeping it true

The baseline is the C++ reference (`roring4rk/roring-rathena`, vanilla pre-re behaviour) and our
own config (`config.template.json` vs rAthena defaults). To re-derive the difference list, diff our
`config/` against the reference `db/` and walk the backlog issues tagged `area:*`.

## Maintenance rule

A PR that changes player-visible behaviour **must** add its wiki entry (or open a wiki issue) as part
of "done". See `roring4rk/ragnarok` AGENTS.md and the `ragnarok-backlog` skill.

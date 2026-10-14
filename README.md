<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. Replaces upstream FilmCraft's README. -->
<p align="center">
  <img src="assets/app-icon/freeandiy-film-1024.png" width="128" alt="FreeANDIY Film icon">
</p>

<h1 align="center">FreeANDIY Film</h1>

<p align="center">
  <b>A free, open-source non-linear video editor. Native Rust, runs on macOS, Windows, Linux and in the browser.</b><br>
  Part of <a href="https://freeandiy.freeandy.agency">FreeANDIY</a>, free creative and office apps by Free Andy Agency.
</p>

---

## About

FreeANDIY Film edits video: a multi-track timeline, trimming tools, effects and transitions,
colour correction and scopes, audio mixing, captions, and export to common formats. It is a native
egui/wgpu app (no webview), and the web version is the same Rust code compiled to WebAssembly.

Every action is a command, so the app can be driven from a CLI (`freeandiy-film-cli`), a JSON
control channel or an MCP server.

**FreeANDIY Film is based on the open-source project
[FilmCraft](https://github.com/storytold/filmcraft) (© ArtCraft Team and contributors,
MIT/Apache-2.0). FreeANDIY is not affiliated with the ArtCraft team.** The editor itself is their
work; FreeANDIY adds its own branding, packaging and translations, and follows upstream closely.

## Download

Builds for macOS, Windows and Linux are published on the
[Releases](https://github.com/FreeAndy21/freeandiy-film/releases) page as
`freeandiy-film-<version>-<os>-<arch>.*`.

## Build from source

Requires Rust (see `rust-version` in `Cargo.toml`).

```sh
cargo run --release -p filmcraft                         # desktop app (binary: freeandiy-film)
cargo run --release -p filmcraft-cli -- --help           # CLI (binary: freeandiy-film-cli)
cd apps/filmcraft-web && trunk build --release           # web build (WebAssembly)
```

The crate names keep upstream's `filmcraft-*`, and projects keep upstream's format, so upstream
changes merge cleanly and projects open in both. The developer documentation in `docs/` is
upstream's and still says FilmCraft.

## How this fork is made

Everything FreeANDIY changes lives in [`freeandiy/`](freeandiy/): the brand definition
(`branding.toml`, `app.toml`), assets, a handful of small patches and text rules. All other files
are regenerated from upstream FilmCraft by `freeandiy/scripts/regenerate.sh`, so updates from
upstream never conflict. See [`freeandiy/docs/upstream-sync.md`](freeandiy/docs/upstream-sync.md).

Issues with FreeANDIY builds go to
[our tracker](https://github.com/FreeAndy21/freeandiy-film/issues), not to upstream.

## License

The code is licensed, like upstream, under either of [MIT](LICENSE-MIT) or
[Apache-2.0](LICENSE-APACHE) at your option. See [`NOTICE`](NOTICE) and [`ATTRIBUTION.md`](ATTRIBUTION.md)
for third-party material.

The FreeANDIY and Free Andy Agency names, the angel Andy, logos and app icons are © Free Andy
Agency and **not** covered by the code license; see
[`freeandiy/assets/brand/LICENSE-brand.txt`](freeandiy/assets/brand/LICENSE-brand.txt).

<sub>Adobe and Premiere Pro are trademarks or registered trademarks of Adobe Inc. in the United
States and/or other countries. FreeANDIY Film is an independent, open-source project and is not
affiliated with, sponsored by or endorsed by Adobe Inc.; these names are used only to describe the
workflows it is compatible with.</sub>

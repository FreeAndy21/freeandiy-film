<!-- Modified-by: FreeANDIY (Free Andy Agency), 2026. New file, not part of upstream FilmCraft. -->
# FreeANDIY Film: changes from upstream FilmCraft

This file lists what the FreeANDIY fork changes in FilmCraft (Apache-2.0 section 4(b)). The
exact changes are generated from `freeandiy/` (see `NOTICE`); `git diff upstream-main main`
shows every changed file.

## Unreleased

### Branding
- Product name **FreeANDIY Film** everywhere users see it: window title, menus, About, the Home
  screen, messages, translations, installers, desktop entries, the CLI.
- Application id `agency.freeandy.film` (was `ai.storyteller.filmcraft`), so FreeANDIY builds
  install next to FilmCraft.
- Executables `freeandiy-film` and `freeandiy-film-cli`; the cargo packages keep their names.
- New app icon set (the angel Andy, Free Andy Agency), the FreeANDIY wordmark in About and on the
  Home screen, and a new DMG background.
- The three themes keep their neutral greys (video is judged against them) with FreeANDIY's
  stamp-rose accent, nearly square windows and no soft shadows.
- UI font IBM Plex Sans (OFL 1.1) on the desktop, upstream's Inter as its fallback.

### Removed
- The ArtCraft name, wordmark and logos (`docs/brand/`, About, Home), as their terms require of
  forks.
- The ArtCraft Discord button and links (header, Help menu, macOS app menu, About, Home).
- Upstream's release and platform workflows.

### Added
- About: attribution to upstream FilmCraft and the Free Andy Agency seal.
- Slovak user interface (menus and common labels; the rest stays English for now).
- `NOTICE` section and `ATTRIBUTION.md` rows for FreeANDIY's assets and fonts; packages now ship
  `NOTICE`, `ATTRIBUTION.md`, the font licences and the brand terms.

# Marko Boško — CV

Live: **https://markoboskoauroville.github.io/markoboskocv/**

Bilingual (HR / EN) portfolio and curriculum vitae. Croatian is the default language.

## Structure

Seven hash-routed tabs inside one file:

| route | area |
|---|---|
| `#/` | Overview, career timeline, entry points |
| `#/tv` | Broadcast and post production |
| `#/film` | Film and documentary |
| `#/ritam` | Rhythm, music, DJ Mantra, Sun Moon Yoga |
| `#/vizual` | Visual work gallery |
| `#/kod` | Code and tools |
| `#/kontakt` | Contact, links, portraits |

## Technical notes

* One static `index.html`. No framework, no bundler, no build step, no dependencies, no tracking.
* Bilingual dictionary compiled into the page as a plain JS object, 124 keys, both languages complete.
* Language persisted in `localStorage` with a first-party cookie fallback. Default is Croatian.
* Hash routing, so deep links like `#/ritam` are shareable and the back button works.
* Career timeline rendered as a five track non linear editing sequence from a single data array.
* Gallery with keyboard accessible lightbox: arrow keys to move, Escape to close.
* Dark UI. No blur, no backdrop-filter.
* Responsive to 360px, visible keyboard focus, `prefers-reduced-motion` respected, print stylesheet included.
* Every image carries explicit `width`/`height` and lazy loading, so nothing shifts or stretches on load.

## Images

Optimised web copies live in `assets/`, sorted by area:

```
live-1..3     live stream and event setups   -> #/tv
film-1..5     production stills              -> #/film
dj-1          DJ Mantra                      -> #/ritam
mus-1..5      music and performance          -> #/ritam
art-1..16     visual work                    -> #/vizual
por-1..9      portraits                      -> #/kontakt
headshot      hero portrait                  -> #/
```

The original full resolution uploads remain in the repository root.

## Editing content

All copy lives in the `DICT` object in the `<script>` block, keyed by `data-i18n` and `data-i18n-html` attributes. Timeline entries live in `CLIPS`, galleries in `GAL`, and the overview cards in `ENTRIES`. Adding a language means adding one key to `DICT` and one button to the `.lang` group.

## Contact

marko.bosko@gmail.com

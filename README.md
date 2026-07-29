# Marko Boško — CV

Live: **https://markoboskoauroville.github.io/markoboskocv/**

Bilingual (HR / EN) curriculum vitae for Marko Boško: video editor, filmmaker, sound engineer, percussionist, DJ, yoga and rhythm teacher.

## Technical notes

* One static `index.html`. No framework, no bundler, no build step, no dependencies.
* Bilingual dictionary compiled into the page as a plain JS object. Switching is instant, no reload, no second URL.
* Language choice persisted in a first-party cookie (`mb_lang`, one year). First visit falls back to browser locale.
* Career timeline rendered as a five track non linear editing sequence, driven by a single data array. Clips are focusable buttons with an inspector panel.
* Dark UI. No blur, no backdrop-filter.
* Responsive to 360px, visible keyboard focus, `prefers-reduced-motion` respected, print stylesheet included.
* No analytics, no trackers, no third party scripts. Fonts from Google Fonts only.

## Structure

```
index.html            entire site: markup, styles, dictionary, timeline data
assets/portrait.jpg
assets/hibiscus.png
```

## Editing content

All copy lives in the `DICT` object near the top of the `<script>` block, keyed by `data-i18n` and `data-i18n-html` attributes in the markup. Timeline entries live in the `CLIPS` array below it. Adding a language means adding one more key to `DICT` and one more button to the `.lang` group.

## Contact

marko.bosko@gmail.com

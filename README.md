Jacquard Documentation
======================

The user guide for [Jacquard], published with GitHub Pages. It is a static site with
no build step: the pages are hand-written HTML and one stylesheet, so what is in the
repository is what is served.

[Jacquard]: https://github.com/keijiro/Jacquard

| | |
| --- | --- |
| `index.html` | The guide. It covers the whole app, section by section |
| `privacy.html` | The privacy policy, from `PRIVACY.md` in the Jacquard repository |
| `assets/style.css` | The whole design, and where the reasoning behind it is written |
| `assets/figures/` | The score figures, copied from `Docs/Figures/` in the Jacquard repository |
| `.nojekyll` | Serve the files as they are rather than running them through Jekyll |

The look is the app's own: the palette is the grey ramp in `Assets/Jacquard/UI/Style.cs`,
and the ground is the score plane's lattice at the pitch the app draws it. Headings,
labels and links are set in Jura, which is the face the interface itself is set in, and
Space Grotesk carries the prose — the one thing here that is read rather than looked at.
Both come from Google Fonts.

Where the text comes from
-------------------------

The Jacquard repository's own documents, carried over by hand: `Docs/manual.md` for the
gestures and the panels, `Docs/sequencer-spec.md` for what the tiles mean, and the
`Docs/impl-*.md` notes for the synth, the mix, the effects and the files. Basic Concepts
is still the README's own prose. Nothing here is invented — when the app changes, the
change is carried over rather than restated.

The pictures the guide asks for are not all taken yet. Each missing one stands as a
dashed placeholder saying what the picture is of, so a file can be dropped in later
without anything around it moving; `.placeholder` in the stylesheet is what draws them.
They are of two kinds, and the two are taken different ways:

- **Screenshots of the app** — the whole screen and the panels. Six of them, all pending
- **Score figures** — a plane cropped to a score's own bounds, the way the twelve in
  `assets/figures/` were taken. Five more are asked for in Inside a Score; the procedure,
  and the `.jacquard` file each existing figure is a picture of, are in `Docs/Figures/`
  in the Jacquard repository

Publishing
----------

GitHub Pages, serving the default branch from the repository root. There is nothing to
build or run first.

To read it locally, open `index.html` in a browser, or serve the folder:

```
python3 -m http.server
```

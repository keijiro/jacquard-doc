Jacquard Documentation
======================

The user guide for [Jacquard], published with GitHub Pages. It is a static site with
no build step: the pages are hand-written HTML and one stylesheet, so what is in the
repository is what is served.

[Jacquard]: https://github.com/keijiro/Jacquard

| | |
| --- | --- |
| `index.html` | The guide. Its text currently comes from the Jacquard README |
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

Everything on the pages is the Jacquard repository's own prose rather than a paraphrase
of it. When the source is changed, the change is carried over here by hand.

Publishing
----------

GitHub Pages, serving the default branch from the repository root. There is nothing to
build or run first.

To read it locally, open `index.html` in a browser, or serve the folder:

```
python3 -m http.server
```

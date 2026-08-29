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
| `assets/screens/` | The screenshots of the app, taken the way the note below says |
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

Where the pictures come from
----------------------------

Both kinds are taken in the editor, in play mode, at a panel scale of 2 — so a UI pixel
is two device pixels, and each one is asked for at half its pixel width. That is what
keeps the interface on this page drawn at the size the interface is drawn at, and sharp
on a display that has the pixels for it.

- **Score figures** (`assets/figures/`) — the plane cropped to a score's own bounds plus
  a margin of ten units, which is what leaves the lattice dots room around the tiles.
  Each is a picture of one `.jacquard` file written for it and nothing else; those files
  and the procedure are in `Docs/Figures/` in the Jacquard repository. `01` to `12` are
  the ones the Jacquard README illustrates the tile rules with; `13` to `17` are this
  guide's own
- **Screenshots** (`assets/screens/`) — the whole screen, and each panel cropped to its
  own bounds plus the same margin of ten, since what tells a panel from the plane is the
  air around it. The visualizer is off for the panel crops: silent it draws one flat
  line across the middle of the screen, and a line through the margin of a crop reads as
  an artefact rather than as the app. It is on for the whole screen, where it *is* the
  app. The whole screen is taken at 880 by 640 units, which is very nearly the narrowest
  the transport row fits across — a screen wider than that is a picture of the app shown
  smaller than the app, and this page has 832 pixels to put it in

Three of them carry labels — the whole screen, the parts of a lane, and the nine tiles —
because the paragraph beside each of those names what it points at. The labels are not
drawn on afterwards: they go on the screen as one more layer of the app's own interface,
set in Jura in the caption grey, with leaders in axis-aligned segments the way the plane
draws a jump link, and are captured with everything else. So the ink in a label is the
ink the app would have used.

The two figures set their labels at the caption size, which is what the app would have
set them at. The whole screen sets its own at 14 units instead, half again as large as
the chrome around it, because a label there is not one more thing on the screen being
described: it is the page speaking about the picture, and it is read at the size this
page's own captions are read at rather than at the size the app's are.

Publishing
----------

GitHub Pages, serving the default branch from the repository root. There is nothing to
build or run first.

To read it locally, open `index.html` in a browser, or serve the folder:

```
python3 -m http.server
```

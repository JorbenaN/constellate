# Constellate

Type, and your letters are built out of stars. They fly in, snap into the shape of each letter and link up into constellations. Push them with your pointer, send a shockwave, or let a shooting star through.

One plain HTML file: canvas and vanilla JavaScript, no build step, no dependencies. Open `index.html` in a browser.

## Controls

| Input | What it does |
| --- | --- |
| Type | Lights up stars that form each letter |
| Space | Sends a shooting star; the word you just finished flares |
| Backspace | Scatters the last letter into dust |
| Enter | Clears everything |
| Click / tap | Shockwave |
| Tab (or the swatches) | Changes the sky |
| PNG / SVG / REC | Export an image, a transparent SVG of just the lettering, or a video |
| Copy code | Copies the page source with a short prompt, ready to paste into Claude |

## How it works

Each glyph is drawn to an offscreen canvas and sampled on a jittered grid. Every sample that lands on ink becomes a star with a spring pulling it to its spot. Stars within a short distance of each other are joined by lines, found with a spatial hash so it stays at 60 fps.

Letters: Unbounded (Google Fonts). Interface: JetBrains Mono.

Made by JRBN.

## License

MIT, see [LICENSE](LICENSE).

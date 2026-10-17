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
| Tab (or the swatches) | Changes the sky (14 palettes, including two light ones) |
| SOUND | Listen through your microphone or a shared tab/screen with audio, and the whole sky reacts (see below) |
| PNG / SVG / REC | Export an image, a transparent SVG of just the lettering, or a video |
| Copy code | Copies the page source with a short prompt, ready to paste into Claude |

## Sound

Each part of the spectrum drives its own effect:

| Range | Effect |
| --- | --- |
| Kick / sub-bass | Camera push and shake, letters hop one after another, shockwave ring |
| Low-mids | Letters glow, soft nebula clouds drift behind |
| Mids / vocals | Aurora curtains across the top, constellation lines shift colour |
| Snare | Meteors fall through the text and burst where they land, stars flash |
| Presence | Four-point sparkles on the background stars |
| Hi-hats / air | Falling glitter, glints and thin fast streaks |
| Whole spectrum | A ring of ticks around the text |

Loud passages add small meteor showers. If the page runs slowly with sound on, it drops the clouds and aurora by itself.

## Earlier versions

The `versions/` folder keeps every earlier build, each a standalone HTML file: `v1-original-no-sound`, `v2-basic-sound`, `v3-immersive-sound`, `v4-14-skies`, plus `type-garden-remake`. The site itself is the `index.html` at the root.

## How it works

Each glyph is drawn to an offscreen canvas and sampled on a jittered grid. Every sample that lands on ink becomes a star with a spring pulling it to its spot. Stars within a short distance of each other are joined by lines, found with a spatial hash so it stays at 60 fps.

Letters: Unbounded (Google Fonts). Interface: JetBrains Mono.

Made by JRBN.

## License

MIT, see [LICENSE](LICENSE).

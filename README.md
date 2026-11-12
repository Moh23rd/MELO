# Melo

A local-first music player for the web — works on desktop and mobile, and your
music never leaves your device.

## What it is

Melo plays audio files straight from your own device. You point it at a folder
or pick files, and the browser reads and plays them locally. There is no upload,
no account, and no tracking.

Melo is a single-page app that also installs as a PWA and keeps its app shell
available offline through a service worker. Playback itself always reads from
your device.

## Goals

- Local playback with zero uploads — audio is read from disk, in the browser.
- A library view that stays quick with large collections.
- One responsive interface that works on phones, tablets and desktops.
- Small and dependency-free, so it is easy to run, host and extend.

## Running it

Melo is a static web app: plain HTML, CSS and JavaScript with no build step.

Serve the repository over HTTP and open it in a modern browser:

```bash
# any static file server works
npx serve .
# or
python3 -m http.server 3000
```

Open <http://localhost:3000>. Some browser APIs used for reading a folder
(File System Access) require `localhost` or HTTPS.

## Deployment

Every push to `main` deploys the static files to GitHub Pages through
`.github/workflows/pages.yml`:

**https://moh23rd.github.io/Melo/**

The app uses relative paths, so it works both at the repository root and under
the `/Melo/` Pages path.

## Project layout

```text
.
├── index.html            # the app: markup, styles and logic
├── manifest.webmanifest  # installable PWA metadata
├── sw.js                 # service worker (offline app shell)
├── icon-*.png            # app icons
├── apple-touch-icon.png  # iOS home screen icon
├── .github/              # CI, Pages deployment, issue and PR templates
├── CONTRIBUTING.md       # how to work on the project
├── LICENSE               # GPL-3.0
└── README.md
```

## Browser support

| Browser                 | Notes                                            |
| ----------------------- | ------------------------------------------------ |
| Chrome / Edge (desktop) | Full support, including linking a folder         |
| Safari (macOS / iOS)    | Playback and file picking                        |
| Firefox                 | Playback and file picking                        |
| Chrome (Android)        | Playback and file picking                        |

## Contributing

Bug reports and feature requests are welcome — see the issue templates, and read
[CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

Melo is free software, licensed under the
[GNU General Public License v3.0](LICENSE).

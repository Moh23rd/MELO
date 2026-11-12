# Melo

A local-first music player for the web — works on desktop and mobile, and your
music never leaves your device.

> **Status:** early. The repository is set up, and the player itself is in
> progress.

## What it is

Melo plays audio files straight from your own device. You point it at a folder
or pick files, and the browser reads and plays them locally. There is no upload,
no account, and no tracking.

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

Some browser APIs used for reading a folder (File System Access) require
`localhost` or HTTPS.

## Project layout

```text
.
├── .github/          # CI, issue and pull request templates
├── CONTRIBUTING.md   # how to work on the project
├── LICENSE           # GPL-3.0
└── README.md
```

The app files will live at the repository root once they are added.

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

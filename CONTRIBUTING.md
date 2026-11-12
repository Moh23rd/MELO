# Contributing to Melo

Thanks for taking a look. This guide covers the practical bits.

## Reporting bugs

Open an issue with the bug report template. Include:

- what you expected and what happened instead,
- the steps that reproduce it,
- your browser, OS and device,
- the audio format (MP3, FLAC, M4A…) if playback is involved.

Please remove personal information from logs and screenshots.

## Suggesting features

Open a feature request describing the problem you want solved. Melo aims to stay
small and local-first, so proposals that add accounts, uploads or tracking are
unlikely to fit.

## Development

Melo is a static site with no build step. Serve the project folder over HTTP:

```bash
python3 -m http.server 3000
# or
npx serve .
```

Then open <http://localhost:3000>. Keep changes working without a bundler.

## Code style

- Plain modern JavaScript (ES modules), no framework unless the project adopts
  one deliberately.
- Two-space indentation, semicolons, double quotes.
- Keep files focused; prefer small modules with clear responsibilities.
- Match the naming and structure of the surrounding code.

## Pull requests

- Keep a pull request scoped to one change.
- Describe the change, how you tested it, and which browsers/devices you tried.
- Link the related issue where there is one.
- Do not commit secrets, personal data, or large media files.

## Commits

Write short, imperative commit subjects, for example:

```text
Add keyboard shortcuts to the player
Fix duration shown for variable bitrate files
```

## License

By contributing, you agree that your contributions are licensed under the
project's GPL-3.0 license.

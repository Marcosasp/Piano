# 🎹 Piano Keyboard

> An interactive piano keyboard playable via keyboard, mouse, or touch — built with Pug, Stylus and Webpack.

[![License](https://img.shields.io/github/license/marcosantonio/piano.svg)](./license)
[![Version](https://img.shields.io/badge/version-2.2.0-blue.svg)](./package.json)

**Live demo:** [piano.marcosantonio.com](https://piano.marcosantonio.com/)

---

## Features

- **Three input modes** — keyboard shortcuts, mouse click, and touchscreen tap
- **Two full octaves** displayed (14 visible keys mapping to 24 audio samples)
- **Progressive Web App** — installable on any device, works offline via Service Worker
- **Fully responsive** — from 380 px mobile up to large desktop screens
- **Real audio samples** — 24 MP3 files covering notes from C (261 Hz) to B (987 Hz)
- **Visual feedback** — keys animate and glow on every press

---

## Tech Stack

| Layer       | Technology                                                         |
| ----------- | ------------------------------------------------------------------ |
| Templating  | [Pug](https://pugjs.org/)                                          |
| Styling     | [Stylus](https://stylus-lang.com/) + PostCSS                       |
| CSS plugins | Autoprefixer · Lost · Rucksack · Font Magician · cssnano           |
| JavaScript  | Vanilla ES6+ compiled with [Babel](https://babeljs.io/)            |
| Audio       | [Howler.js](https://howlerjs.com/)                                 |
| Bundler     | [Webpack 5](https://webpack.js.org/)                               |
| PWA         | [Workbox](https://developer.chrome.com/docs/workbox/) (GenerateSW) |
| Linting     | ESLint · Stylint                                                   |

---

## Prerequisites

- [Node.js](https://nodejs.org/) ≥ 16
- [Yarn](https://yarnpkg.com/) (recommended) or npm

---

## Getting Started

```sh
# Clone the repository
git clone https://github.com/marcosantonio/piano.git
cd piano

# Install dependencies
yarn

# Start the development server
yarn start
```

The dev server starts on `http://localhost:8080` and opens the browser automatically.

---

## Available Scripts

| Command         | Description                        |
| --------------- | ---------------------------------- |
| `yarn start`    | Development server with hot reload |
| `yarn build`    | Production build output to `dist/` |
| `yarn lint`     | Lint JavaScript and CSS            |
| `yarn lint:js`  | Lint JavaScript only (ESLint)      |
| `yarn lint:css` | Lint CSS only (Stylint)            |
| `yarn fix:js`   | Auto-fix ESLint errors             |
| `yarn analyzer` | Build and open bundle size report  |

---

## Keyboard Shortcuts

The keyboard layout follows the piano's white and black key pattern.

| Key         | Note |     | Key   | Note |
| ----------- | ---- | --- | ----- | ---- |
| ⇪ Caps Lock | C    |     | Q     | C#   |
| A           | D    |     | W     | D#   |
| S           | E    |     |       |      |
| D           | F    |     | R     | F#   |
| F           | G    |     | T     | G#   |
| G           | A    |     | Y     | A#   |
| H           | B    |     |       |      |
| J           | C    |     | I     | C#   |
| K           | D    |     | O     | D#   |
| L           | E    |     |       |      |
| ;           | F    |     | [     | F#   |
| '           | G    |     | ]     | G#   |
| \           | A    |     | Enter | A#   |
| ←           | B    |     |       |      |

---

## Project Structure

```
piano/
├── src/
│   ├── js/
│   │   └── piano.js          # Core logic (audio, keyboard, touch events)
│   ├── styl/
│   │   ├── variables.styl    # Colors, spacing, breakpoints
│   │   ├── base.styl         # Global reset and base styles
│   │   ├── typography.styl   # Headings and text styles
│   │   ├── piano.styl        # Piano keyboard component
│   │   ├── main.styl         # Main content area
│   │   ├── footer.styl       # Footer styles
│   │   └── app.styl          # Entry point — imports all partials
│   ├── medias/               # 24 MP3 audio samples (261 Hz – 987 Hz)
│   ├── images/               # App icon
│   ├── index.pug             # HTML template
│   └── app.js                # JS entry point
├── dist/                     # Production build (generated)
├── app.config.json           # App metadata (title, URL, theme color)
├── webpack.config.js         # Webpack configuration
├── postcss.config.js         # PostCSS plugins
├── package.json
└── license
```

---

## License

MIT License © [Marcos Antônio](https://twitter.com/marcosantonio_)

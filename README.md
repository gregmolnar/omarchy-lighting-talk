# Omarchy — presentation

A reveal.js deck about Omarchy, themed to match it.

## Run

Open `index.html` in a browser. No build step, no server.

```bash
xdg-open index.html
```

A server is only needed if you later split slides into external Markdown files,
which `fetch()` can't load over `file://`:

```bash
npm start          # http://localhost:8000
```

Speaker notes: press `S`. Overview: `Esc`. Print to PDF: append `?print-pdf`
to the URL and print from Chromium.

## Structure

```
index.html        the slides
css/omarchy.css   the theme
img/              assets (omarchy logo)
```

## Theming

`css/omarchy.css` declares the same colour tokens an Omarchy theme does, so
re-skinning the deck is a copy of any `colors.toml`:

```bash
cat ~/.local/share/omarchy/themes/<name>/colors.toml
```

Paste those values into `:root`. Three alternates ship as body classes —
`theme-catppuccin`, `theme-gruvbox`, `theme-matte-black`:

```html
<body class="theme-gruvbox">
```

## Slide helpers

| Class        | Use                                             |
|--------------|-------------------------------------------------|
| `.title`     | Title slide — logo, tagline, prompt line        |
| `.statement` | Big centred one-liner                           |
| `.label`     | Small uppercase kicker above a heading          |
| `.prompt`    | Line prefixed with a `❯` shell prompt           |
| `.cursor`    | Blinking block cursor                           |
| `.window`    | Bordered box, like a tiled Hyprland client      |
| `.tiles`     | Auto-fitting grid wrapper for `.tile` cards     |

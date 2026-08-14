# Rashid Charcoal Material

A dark, Material Design–inspired theme for Thunderbird in charcoal grey tones with a subtle blue-grey (Blue Grey 500/600) accent palette.

![Theme](bird_PO.png)

## Features

- Full charcoal grey (`#212121` / `#2E2E2E` / `#263238`) dark UI across the main window, folder pane, message list, and calendar
- Blue-grey accent colors (`#546E7A`, `#78909C`, `#90A4AE`) for highlights, selection, and hover states
- Themed spaces toolbar (left sidebar) with active/inactive button states
- Styled calendar views: month grid, today/weekend highlighting, task and agenda backgrounds
- Custom message pane styling, including a themed default/initial message background image
- Built using Thunderbird's `theme_experiment` API for deeper styling beyond the standard `theme.colors` surface (folder pane counts, message list header, calendar internals, etc.)

## Compatibility

| | |
|---|---|
| Thunderbird version | 115.0 – 141.* |
| Manifest version | 2 |
| Theme type | `theme_experiment` (static + experimental CSS variables) |

## Installation

1. Download the latest `.xpi` file (or clone this repo and zip the contents).
2. In Thunderbird, go to **Menu → Add-ons and Themes** (or `Ctrl+Shift+A`).
3. Click the gear icon (⚙) and choose **Install Add-on From File...**
4. Select `Rashid-Charcoal-Material.xpi`.
5. Enable the theme from the **Themes** tab.

## Building from source

```bash
# From the repository root
zip -r Rashid-Charcoal-Material.xpi manifest.json style.css *.png Icons/
```

## Project structure

```
.
├── manifest.json     # Theme manifest & theme_experiment color/property mappings
├── style.css          # Experimental CSS variable stylesheet
├── cheese64.png        # Theme icon
├── bird_PO.png          # Initial/default message pane image
└── Icons/                # Icon set used by the theme
```

## Customization

Colors are defined in two places in `manifest.json`:

- `theme.colors` – standard Thunderbird theme API colors
- `theme_experiment.colors` (mapped to CSS custom properties) – extended styling consumed by `style.css`, covering things like folder pane counts, calendar backgrounds, and message list styling

To create your own variant, fork this repo and adjust the hex values in `manifest.json`, then update `style.css` if you add or rename any CSS variables.

## Author
**Rashid Sohaib**

## License
MIT

# notion-embeds

Small single-file HTML widgets meant to be embedded in Notion pages with `/embed`. No build step and no dependencies. Each widget follows the system light or dark theme.

| Widget | File | What it shows |
|---|---|---|
| Clock | `clock.html` | Analog clock face (Los Angeles time unless you set another zone) |
| Calendar | `calendar.html` | Month grid with today marked, Sunday-first |

`index.html` lists the widgets.

## Options

Both widgets are configured with URL query parameters:

| Param | Widgets | Example | Effect |
|---|---|---|---|
| `color` | both | `color=448361` | Accent color (hex without `#`, or any CSS color) |
| `fill` | both | `fill=false` | Card background: on by default (accent), `false` for transparent, or a color |
| `tz` | both | `tz=Asia/Seoul` | Time zone |
| `zones` | clock | `zones=America/Los_Angeles,Asia/Seoul` | Zones to cycle through on click |
| `date` | clock | `date=true` | Show the date in the dial |
| `seconds` | clock | `seconds=needle` | Seconds as `arc` (default), `needle`, or `off` |
| `start` | calendar | `start=mon` | Week starts on Monday |
| `month` | calendar | `month=2026-10` | Show a specific month |

## Using one

The widgets are live on GitHub Pages at [techo10n.github.io/notion-embeds](https://techo10n.github.io/notion-embeds/). Paste a widget's URL, with any options, into a Notion `/embed` block, for example:

```
https://techo10n.github.io/notion-embeds/clock.html?zones=America/Los_Angeles,Asia/Seoul&date=true
```

# Journal — Quadrant

A minimal, typography-heavy newsletter theme for [Ghost](https://github.com/TryGhost/Ghost), skinned to the **Quadrant UI** design system.

Built on TryGhost's [Journal](https://github.com/TryGhost/Themes) theme, this variant reskins the theme to match Quadrant — the dark, slate-based design language of the [Quadrant](https://claude.ai/design/p/ff456d7a-1ec1-478b-b934-dd85a6b89139) modpack manager.

## Design language

- **Dark slate surfaces** — slate-900 page background, slate-800 cards and inputs, slate-50 / slate-400 text.
- **Blue primary actions** — blue-600 fills (blue-400 for small accent text such as dates, tags, and links), emerald for positive actions, red for destructive.
- **Pills everywhere** — buttons, inputs, and the subscribe card use fully rounded (`rounded-full` / `rounded-4xl`) corners.
- **Inter typeface** — regular body text with **extrabold (800)** buttons.

The design tokens live in `assets/css/screen.css` (`:root`), with hex values taken from the Quadrant design project's color reference. Ghost's admin-set accent color overrides the blue-600 fallback in production — set the site accent to `#155DFC` to keep Portal and emails on-palette.

> [!NOTE]
> Upstream Journal is developed in the [TryGhost/Themes](https://github.com/TryGhost/Themes) monorepo. This repo intentionally diverges from upstream to carry the Quadrant skin.

# Instructions

1. [Download this theme](https://github.com/TryGhost/Journal/archive/main.zip)
2. Log into Ghost, and go to the `Design` settings area to upload the zip file

# Development

Styles are compiled using Gulp/PostCSS to polyfill future CSS spec. You'll need [Node](https://nodejs.org/), [pnpm](https://pnpm.io/) and [Gulp](https://gulpjs.com) installed globally. After that, from the theme's root directory:

```bash
# Install
pnpm install

# Run build & watch for changes
pnpm dev
```

Now you can edit `/assets/css/` files, which will be compiled to `/assets/built/` automatically.

The `zip` Gulp task packages the theme files into `dist/journal.zip`, which you can then upload to your site.

```bash
pnpm zip
```

Remember to rebuild (`pnpm dev` or `gulp build`) so `assets/built/` stays in sync after editing source CSS/JS.

## Theme translations

Please see the @Tryghost/Themes/theme-translations/README.md for how to edit or contribute translations.

# Copyright & License

Copyright (c) 2013-2026 Ghost Foundation - Released under the [MIT license](LICENSE).

# Umbrel Apps Gallery

Icons and gallery images for [zot24's Umbrel Community App Store](https://github.com/zot24/umbrel-apps).

## Why This Repository Exists

Umbrel community app stores have a known limitation where icons and gallery images placed directly in the app folder don't display correctly. The Umbrel UI fetches assets from the official gallery endpoint rather than the community store repository.

**The workaround**: Host assets in a separate repository and reference them via full raw GitHub URLs in `umbrel-app.yml`.

This issue is tracked at [getumbrel/umbrel#1998](https://github.com/getumbrel/umbrel/issues/1998).

## Structure

```
umbrel-apps-gallery/
└── <app-id>/
    ├── icon.svg      # 256x256 app icon (SVG)
    ├── 1.png         # Gallery image (1440x900)
    ├── 2.png
    └── ...
```

## Usage in umbrel-app.yml

Reference assets using raw GitHub URLs:

```yaml
icon: https://raw.githubusercontent.com/zot24/umbrel-apps-gallery/main/<app-id>/icon.svg
gallery:
  - https://raw.githubusercontent.com/zot24/umbrel-apps-gallery/main/<app-id>/1.png
  - https://raw.githubusercontent.com/zot24/umbrel-apps-gallery/main/<app-id>/2.png
  - https://raw.githubusercontent.com/zot24/umbrel-apps-gallery/main/<app-id>/3.png
```

## Apps

| App ID | Icon | Gallery |
|--------|------|---------|
| zot24-hermes | [icon.svg](zot24-hermes/icon.svg) | [1](zot24-hermes/1.png), [2](zot24-hermes/2.png), [3](zot24-hermes/3.png), [4](zot24-hermes/4.png), [5](zot24-hermes/5.png) |

## Related Repositories

- [zot24/umbrel-apps](https://github.com/zot24/umbrel-apps) - App definitions and docker-compose files
- [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) - Hermes Agent by Nous Research

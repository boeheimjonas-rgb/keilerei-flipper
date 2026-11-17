# KEILEREI – App Manifest

| Field | Value |
|---|---|
| App ID | `keilerei` |
| Name | Keilerei |
| Version | 1.0 |
| Category | Games |
| Author | JB |
| Entry point | `keilerei_app` |
| Type | External app (FAP) |
| Target / API | f7, built against official firmware 1.5.1 (API 88.2) |
| Requires | gui, storage, notification |
| Stack | 4 KB |
| RAM | ~3 KB game state + 1 KB framebuffer |
| Icon | `keilerei.png` (10×10, 1-bit) |
| Source | https://github.com/boeheimjonas-rgb/keilerei-flipper |
| License | MIT |
| Data stored | High score only: `/ext/apps_data/keilerei/hiscore.bin` |
| Network | none |

## Files
| File | Purpose |
|---|---|
| `application.fam` | Flipper build manifest (ufbt/fbt) |
| `manifest.yml` | Manifest for the official Flipper Apps Catalog |
| `fight_core.c/.h` | Game core (C99, platform-independent) |
| `fight_app.c` | Flipper glue code |
| `font.inc` | 3×5 pixel font |
| `web/index.html` | Browser/Android version (same logic) |
| `screenshots/` | 128×64 screenshots for the catalog |

## Publishing to the Flipper Apps Catalog
1. Fork https://github.com/flipperdevices/flipper-application-catalog
2. Copy `manifest.yml` to `applications/Games/keilerei/manifest.yml` and set `commit_sha` to the commit you want to publish.
3. Open a pull request. The catalog CI builds the app and checks the manifest.

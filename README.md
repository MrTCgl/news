# news

In-app announcements for MrTCgl's apps. Each app reads its own file at start:

| App | File | URL the app reads |
|---|---|---|
| LingoBall | `lingoball.json` | https://raw.githubusercontent.com/MrTCgl/news/main/lingoball.json |
| NabKap | `nabkap.json` | https://raw.githubusercontent.com/MrTCgl/news/main/nabkap.json |
| DurakBul | `durakbul.json` | https://raw.githubusercontent.com/MrTCgl/news/main/durakbul.json |

## Format

```json
{
  "id": "2026-11-03-1",
  "text": {
    "en": "Try DurakBul, find your stop in seconds",
    "tr": "DurakBul'u dene, durağını saniyede bul",
    "de": "...", "fr": "...", "es": "...", "it": "..."
  },
  "url": "https://play.google.com/store/apps/details?id=..."
}
```

- `id` empty → nothing is shown.
- A new announcement needs a new `id`. Once a user closes or opens it, that `id` is never shown to them again.
- `text`: the app shows the user's own language and falls back to `en`.
- `url` is optional. If set, tapping the card opens it.
- Keep it short (one line, about 50 characters) and calm.

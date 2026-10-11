# Deep-Live-Cam No-NSFW

This branch keeps the original Deep-Live-Cam behavior, but changes NSFW filtering to an explicit opt-in switch.

Default behavior:
- NSFW filtering is OFF by default
- You can enable it via CLI flag or env var
- No hardcoded content filtering runs unless enabled

## Quick start

1. Copy `.env.example` to `.env`
2. Set `ENABLE_NSFW_FILTER=false` to keep it off by default
3. Run the app normally

Optional:

```bash
python run.py --nsfw-filter
```

Or:

```bash
ENABLE_NSFW_FILTER=1 python run.py
```

## Why this is safer

This keeps the original project structure but makes moderation behavior configurable instead of always enforced.

## Files added

- `modules/globals.py`
- `modules/core.py`
- `.env.example`

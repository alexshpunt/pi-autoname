# pi-autoname

This is alexshpunt's fork of `ssdiwu/pi-autoname`. It names Pi sessions in English kebab-case by default, without a length cap. `README.md` describes the triggers and configuration.

- Names come from the meaning of the session and stay stable between renames. Never use a raw model answer as a name.
- A user's `/name` is replaced only as `respectManualName` allows.
- Session content and generated titles are private: don't log them, don't send them to a provider the user hasn't configured, and don't persist extra prompts.
- Use Pi's configured model and credentials. Never hardcode a provider, model or key.
- Automatic naming and `/autoname` share one naming core. Concurrent or repeated triggers are deduplicated, and a model failure falls back without breaking the session.

## Checks

Run `npm test`. When triggers or Pi API usage change, load this checkout in Pi and check automatic naming, `/autoname`, the state after `/reload`, and the fallback when the model fails. Say so when no real model was used.

Update `README.md` and `CHANGELOG.md` when triggers, configuration, privacy boundaries or installation change.

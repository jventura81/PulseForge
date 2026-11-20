# PulseForge V22.2 — Mobile and PWA candidate

## Test
- Desktop: drag/drop remains available.
- Mobile <=900px: tap palette note then tap measure to insert; switch to Multi-select to tap multiple notes; Move mode taps source then destination.
- Tap `+ Add ... to end` below a measure when needed.
- Installable on HTTPS via manifest and service worker. Safari iOS: Share > Add to Home Screen. Chrome Android: browser menu > Install app.
- Offline cache works after first successful online load. Project data remains local to each browser/device, not synchronized.
- Verify real-device touch scrolling, audio playback, imports, backup/export, and share links before launch.
- On mobile, inspect palm-mute controls via Note Inspector.
- The offline service worker caches same-origin assets only; externally linked song resources are not cached.

## Deploy
Upload these files together at the site root. Vercel supports static sites. A custom domain is optional.

## V22.3 diagnostics
A startup banner remains visible if scripts cannot execute; if a synchronous JavaScript exception occurs, it displays the error. This is a debugging build, not a verified mobile fix.

Deploy all files to a testing HTTPS URL, then open directly in mobile Safari/Chrome (not the ChatGPT attachment viewer). Record exact startup error if any.

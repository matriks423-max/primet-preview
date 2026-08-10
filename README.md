# Primet — static preview

Static export of the Primet website for sharing. Live site: **https://primet.pro**

Preview: **https://matriks423-max.github.io/primet-preview/**

## What this is

A build artifact, not source. The source lives in a private repo. This copy exists
only so the design can be shared via a link.

Differences from the live site:

- No server, so the API routes (`/api/chat`, `/api/contact`, `/api/t`) are absent —
  the chat widget, contact form, and analytics beacon are inert here.
- The `/admin` pages are excluded.
- `robots.txt` disallows everything so this copy does not compete with primet.pro
  in search results.

## Rebuilding

From the source repo (`primet2/app`), with `app/api`, `app/admin`, and `proxy.ts`
moved aside:

```
STATIC_EXPORT=true NEXT_PUBLIC_BASE_PATH=/primet-preview npm run build
```

Then commit the contents of `out/` to this repo's `main` branch.

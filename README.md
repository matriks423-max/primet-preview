# Primet — static preview

Static export of the Primet website for sharing. Live site: **https://primet.pro**

Preview: **https://matriks423-max.github.io/primet-preview/**

## What this is

A build artifact, not source. The source lives in a private repo and is published
here automatically by its `Publish static preview` workflow on every push to `main`.
Do not edit this repo by hand — the next build replaces the whole tree.

Differences from the live site:

- No server, so the API routes (`/api/chat`, `/api/contact`, `/api/t`) are absent —
  the chat widget, contact form, and analytics beacon are inert here.
- The `/admin` pages are excluded.
- `robots.txt` disallows everything so this copy does not compete with primet.pro
  in search results.

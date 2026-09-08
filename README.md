# Codriver Radio

A compact music player built for a Codriver widget slot. It follows the iframe contract documented in the [Codriver developer guide](https://developer.codriver.io/en/guides/build-an-app): a `ready` / `context` handshake, dark and light themes, `uiSize`-driven base type, no framework, and a 300 × 130 layout with no scrolling.

## Listen

The widget contains two original Codriver tracks:

- One Corner Ahead
- King of the Morning

Browsers prohibit autoplay, so playback begins only after the driver taps the play button over the cover. A single `>> next` control switches tracks. Use audio controls only while parked.

## Run locally

```sh
npm run serve
```

Open <http://localhost:8794/dev.html>. The harness simulates Codriver's widget host and lets you change theme, text size, and slot dimensions.

## Deploy

```sh
npm install
npm run deploy
```

The Cloudflare Pages project is `playlist-codriver`. Only `public/` is deployed.

## App contract

- Public HTTPS widget URL: <https://playlist-codriver.pages.dev>
- Marketplace manifest: `codriver-app.json`
- No configuration or external APIs
- No analytics, cookies, location, account, or map access
- No `X-Frame-Options` or CSP `frame-ancestors` header

## License

Source code is MIT licensed, copyright 9570-6198 Québec inc. The songs and cover artwork are copyright Codriver and are not included in the MIT license grant.

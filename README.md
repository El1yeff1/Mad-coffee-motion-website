# Mad-coffee-website
A responsive specialty coffee shop website concept with custom visuals, an interactive menu, and an optional admin API.

https://mad-coffee-demo.vercel.app/

# Mad Coffee 

A portfolio concept for a specialty coffee shop website. It is an independent demo and is not affiliated with or endorsed by any real coffee business. Contact details and social handles are examples only; no social or phone links are active.

This repository contains the frontend only. The API server and database are not included. Public pages use local fallback content when the API is unavailable. The admin interface is included as frontend UI, but sign-in and data changes require a separately hosted API.

The frontend does not request live API data by default, so the static demo works without a backend. Set `VITE_API_ENABLED=true` only when `/api/site-data` is routed to a compatible API.

## Run locally

Requirements: Node.js 20+ and pnpm 9+.

```sh
pnpm install
pnpm dev
```

Open the local Vite address shown in the terminal. Build the frontend with `pnpm build`.

## Deploy

The repository root is the project root. Build command: `pnpm build`. Publish/output directory: `artifacts/mad-coffee/dist`.

Vercel settings are included in `vercel.json`; Netlify settings are included in `netlify.toml`. Do not set the project root to `artifacts/mad-coffee`, because the pnpm workspace and frontend client package are at the repository root.

To connect the frontend to an existing API during development, set `VITE_API_ENABLED=true` and `API_PROXY_TARGET` to that API's base URL. For production, configure the host to route `/api` requests to the API service.

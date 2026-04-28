# jobapp

This project is configured to deploy as a static Cloudflare Pages site.

## Cloudflare Pages setup

The site is a single static page served directly from the repository root:

- Build command: none
- Build output directory: `.`

Cloudflare reads that configuration from `wrangler.toml`, so the same setup works in the dashboard and with the CLI.

## Deploy from GitHub

1. Push this repository to GitHub.
2. In Cloudflare, go to Workers & Pages and create a new Pages project.
3. Connect the GitHub repository.
4. Use these build settings:
5. Build command: leave blank
6. Build output directory: `.`
7. Save and deploy.

Every push to `main` will trigger a new Pages deployment.

## Deploy with Wrangler

1. Install dependencies:

```bash
npm install
```

2. Authenticate with Cloudflare:

```bash
npx wrangler login
```

3. Preview locally:

```bash
npm run dev
```

4. Deploy:

```bash
npm run deploy
```

If you want the first CLI deploy to create a named Pages project, run:

```bash
npx wrangler pages project create jobapp
```

Then run the deploy command again.
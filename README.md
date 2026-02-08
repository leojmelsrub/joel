# Joel Burslem Portfolio (Astro + Cloudflare Pages)

## Local dev

```bash
npm install
npm run dev
```

## Configure CTA links

Update `src/lib/site.ts`:

- `ctaPrimary`: "Schedule a Strategy Audit"
- `ctaSecondary`: "Read the Daily Riff"

## Social image

Place the social image at `public/og.jpg` and replace the placeholder when ready.

## Cloudflare Pages (Git integration)

1. Push this repo to GitHub or GitLab.
2. In Cloudflare Dashboard: Workers & Pages -> Create -> Connect to Git.
3. Build settings:
   - Build command: `npm run build`
   - Build output directory: `dist`
   - Root directory: `/`
   - Deploy command: leave blank (Cloudflare Pages handles deploys automatically)
4. Deploy. Cloudflare will auto-build on every push to `main`.

Optional: `wrangler.jsonc` is included with `pages_build_output_dir` set to `./dist`.

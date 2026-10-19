# Scraperize docs (Thally)

Developer documentation for [Scraperize](https://scraperize.com), the REST API that returns public social
media data — profiles, posts, comments and more — as clean JSON. Built and published with
[Thally](https://thally.io).

## What's here

| Path | What it is |
| --- | --- |
| `src/content/` | The pages, as MDX: introduction, quickstart, authentication, platforms, core concepts, FAQ, status, MCP integration |
| `docs.json` | Tabs, sidebar groups, navbar, footer, fonts and the API reference source |
| `openapi.json` | The Scraperize OpenAPI 3 spec; the **API Reference** tab (82 endpoints) is generated from it |
| `src/data/site.ts` | Site name, description and the Scraperize color palette |
| `public/images/` | Logo, favicon and AI-client icons |

Everything else is the Thally runtime, managed by `starter-release.json`. Don't edit it by hand.

## Run locally

Requires Node.js 20+ and npm 11+. The template's scripts assume npm's dependency layout, so pnpm installs
fail, and npm 10.9 crashes resolving this dependency tree (`Cannot read properties of null (reading 'edgesOut')`).
Upgrade with `npm install -g npm@11`, or prefix the install with `npx npm@11`.

```bash
npm install
npm run dev
```

Open [http://localhost:3040](http://localhost:3040).

## Validate before publishing

```bash
npx thally check
npm run build
```

`thally check` catches pages missing from `docs.json`, orphan pages and missing frontmatter.

## Publish

The site is published on Thally Cloud from this repository: in [Thally Cloud](https://app.thally.io), create a
site, choose **Use an existing repository**, and select this repo. Every push to the production branch
builds and publishes a new release.

## License

[MIT](LICENSE)

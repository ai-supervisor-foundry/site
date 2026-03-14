# Foundry — Documentation & Marketing Site

Static site for [Foundry](https://github.com/ai-supervisor-foundry/foundry): documentation, wiki, and product landing.

## Contents

- **Landing** — Product overview and quickstart
- **Docs** — Getting started, architecture, control loop, validation, installation, usage, configuration, task schema, state, recovery, PM2, sandbox
- **Wiki** — Overview, software factory model, core principles, key components, FAQ, context window, logging, recovery, troubleshooting, glossary

## Deploy

This is a static site. Serve the repository root (e.g. GitHub Pages, Netlify, Vercel, or any static host).

- **index.html** at the root
- **assets/** — JS and CSS
- **images/** — Static images

No API or server required.

## Regenerating

The site is built from the [supervisor-website](https://github.com/auto-layer/supervisor-website) monorepo. Use **`BASE_PATH=/site/`** so assets and routes work on GitHub Pages (`https://<org>.github.io/site/`):

```bash
# From supervisor-website root
BASE_PATH=/site/ pnpm --filter @workspace/foundry-site run build
cp -r artifacts/foundry-site/dist/public/* path/to/site/
```

## License

MIT

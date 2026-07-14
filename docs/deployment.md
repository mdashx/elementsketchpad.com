# Deploying elementsketchpad.com

Manual deployment of this Hugo site to **Cloudflare Pages**.

This document assumes:

- canonical host: `www.elementsketchpad.com`
- Cloudflare Pages project: `elementsketchpad`

If the existing Pages project uses a different name, change only the
`--project-name` value in the commands below.

## Build

```bash
cd ~/repos/elementsketchpad.com
rm -rf public
hugo --minify --baseURL "https://www.elementsketchpad.com/"
```

## Deploy

```bash
wrangler pages deploy public --project-name elementsketchpad --branch main
```

## Verify

```bash
curl -sI https://www.elementsketchpad.com/ | head -1
curl -s https://www.elementsketchpad.com/ | grep -o '<title>[^<]*</title>'
```

Expected result: the site returns `200` and the title reflects the current
Element Sketchpad build.

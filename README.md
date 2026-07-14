# Element Sketchpad Site

This repository contains the `elementsketchpad.com` site built with
[Hugo](https://gohugo.io/) and the
[Basic Web Theme](https://www.basicwebtheme.com/).

## Build

From the repo root:

```bash
hugo --minify --baseURL "https://www.elementsketchpad.com/"
```

The generated site is written to `public/`.

## Structure

- `content/` - site pages
- `layouts/` - site-specific Hugo partial overrides
- `static/` - static assets
- `docs/` - deployment notes

---
title: AstroWind
description: The default AstroWind template with some needed modifications
tags:
  - Node
  - Astro 5.0
  - AstroWind
  - TypeScript
---

# AstroWind

This project was originally forked from https://github.com/onwidget/astrowind.

[![Deploy on Railway](https://railway.app/button.svg)](https://railway.com/template/Ic0JBh)

## ✨ Features

- ✅ Production-ready scores in PageSpeed Insights reports.
- ✅ Integration with Tailwind CSS supporting Dark mode and RTL.
- ✅ Fast and SEO friendly blog with automatic RSS feed, MDX support, Categories & Tags, Social Share, ...
- ✅ Image Optimization (using new Astro Assets and Unpic for Universal image CDN).
- ✅ Generation of project sitemap based on your routes.
- ✅ Open Graph tags for social media sharing.
- ✅ Analytics built-in Google Analytics, and Splitbee integration.

## 💁‍♀️ Local Development

- Install required dependencies with `npm install`
- Run `npm run dev` for a local development server
- Navigate to `http://127.0.0.1:4321/`. The application will automatically reload if you change any of the source files.

To get more help on the Astro CLI use go check out the [Astro CLI Overview and Command Reference](https://docs.astro.build/en/reference/cli-reference/) page.

## ❓ What was changed from the default AstroWind example?

#### Useing the Node adapter with the `server` output mode is an easy way to get your Astro site running on Railway effciently.

1. Install the Node adadpter

    `npm i @astrojs/node`

2. Import the Node adapter

    Under the `defineConfig` import line paste the import for the Node adapter.

    `import node from '@astrojs/node';`

3. Set the output to `server` and the host to `0.0.0.0`

    Paste this into the `astro.config.ts` file with the `defineConfig` object -

    ```javascript
    output: 'server',
    adapter: node({
      mode: 'standalone',
    }),

    server: {
      host: '0.0.0.0'
    },
    ```

4. Update the start script

    In the `package.json` set the `start` script to -

    `node ./dist/server/entry.mjs`

    This will start the server in production mode.


Railway will automatically use the `build` and `start` scripts from the package.json.

Thats all the changes needed to deploy an Astro app on Railway!

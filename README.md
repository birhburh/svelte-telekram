# svelte-telekram

A Telegram client for KaiOS using Svelte and TypeScript. Forked from [arma7x](https://github.com/arma7x/svelte-telekram) and developed further for fun.

### Development and testing

`npm run dev` builds the app in watch mode and serves the site. Great for testing your app in a desktop browser.

#### Source code style

The code is automatically styled via prettier. [![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)

`npm run check-format` checks the format of `.ts` and `.svelte` files. `npm run format` reformats the code.

### Deploying to a device

[**Read this before continue**](https://github.com/arma7x/svelte-telekram/issues/2)

1. Connect your device to your computer and make sure it appears in WebIDE.
2. `npm run build`
3. In WebIDE, load the `/public` folder as a packaged app.

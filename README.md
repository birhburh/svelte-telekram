# svelte-telekram

A Telegram client for KaiOS using Svelte and TypeScript. Forked from [arma7x](https://github.com/arma7x/svelte-telekram) and developed further for fun.

### Development and testing

`npm run dev` builds the app in watch mode and serves the site. Great for testing your app in a desktop browser.

#### Source code style

The code is automatically styled via prettier. [![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)

`npm run check-format` checks the format of `.ts` and `.svelte` files. `npm run format` reformats the code.

### Deploying to a device

#### 1. Get your API Id and API Hash from Telegram

1. Get your own `api_id` and `api_hash` at [https://my.telegram.org](https://my.telegram.org). Guide [https://core.telegram.org/api/obtaining_api_id] https://core.telegram.org/api/obtaining_api_id
2. Copy and rename `.env.example` to `.env`
3. Replace the value inside `.env`

#### 2. Deploy the app to your device

1. Connect your device to your computer and make sure it appears in WebIDE.
2. Run `npm run build`
3. In WebIDE, load the `/public` folder as a packaged app.

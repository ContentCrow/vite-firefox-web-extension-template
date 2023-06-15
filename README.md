# Firefox Web Extension Template

This template should help get you started developing Firefox manifest v2 web extension in Vite with Vue.js.
It has tailwindcss and material icons installed.

## Usage Notes

The extension manifest is defined in `src/manifest.js` and used by `@samrum/vite-plugin-web-extension` in the vite config.

Background, content scripts, options, and popup entry points exist in the `src/entries` directory. 

Content scripts are rendered by `src/entries/contentScript/renderContent.js` which renders content within a ShadowRoot
and handles style injection for HMR and build modes.

Otherwise, the project functions just like a regular Vite project.

Refer to [@samrum/vite-plugin-web-extension](https://github.com/samrum/vite-plugin-web-extension) for more usage notes. Thank you @samrum.

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install -g pnpm
pnpm install
```

## Commands
### Build
#### Development, HMR

Hot Module Reloading is used to load changes inline without requiring extension rebuilds and extension/page reloads
Currently only works in Chromium based browsers.
```sh
pnpm dev
```

#### Production

Minifies and optimizes extension build
```sh
pnpm build
```

### Load extension in browser

Loads the contents of the dist directory into the specified browser
```sh
pnpm serve:chrome
```

Run additional to the dev server to get hot reload for firefox
```sh
pnpm serve:firefox
```

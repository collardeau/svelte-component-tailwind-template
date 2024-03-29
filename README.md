# svelte-component-tailwind-template

A base for building shareable Svelte components that includes [tailwindcss](https://tailwindcss.com/). Clone it with [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit collardeau/svelte-component-tailwind-template my-new-component
cd my-new-component
npm install # or yarn
```

Your component's source code lives in `src/index.svelte`.

## Setting up

* Run `npm init` (or `yarn init`)
* Replace this README with your own


## Consuming components

Your package.json has a `"svelte"` field pointing to `src/index.svelte`, which allows Svelte apps to import the source code directly, if they are using a bundler plugin like [rollup-plugin-svelte](https://github.com/rollup/rollup-plugin-svelte) or [svelte-loader](https://github.com/sveltejs/svelte-loader) (where [`resolve.mainFields`](https://webpack.js.org/configuration/resolve/#resolve-mainfields) in your webpack config includes `"svelte"`). **This is recommended.**

For everyone else, `npm run build` will bundle your component's source code into a plain JavaScript module (`index.mjs`) and a UMD script (`index.js`). This will happen automatically when you publish your component to npm, courtesy of the `prepublishOnly` hook in package.json.

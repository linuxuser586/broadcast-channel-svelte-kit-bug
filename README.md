# BroadcastChannel SvelteKit Bug

## Demo

```bash
git clone https://github.com/linuxuser586/broadcast-channel-svelte-kit-bug.git
cd broadcast-channel-svelte-kit-bug
npm i
npm run dev -- --open
```

Observer `process is not defined` error

Clone the patched version of [broadcast-channel](https://github.com/linuxuser586/broadcast-channel/tree/svelte-kit-fixes)

```bash
git clone --branch svelte-kit-fixes https://github.com/linuxuser586/broadcast-channel.git
cd broadcast-channel
npm link
```

Run with patch

```bash
# in broadcast-channel-svelte-kit-bug directory
# clear the vite cache
rm -rf node_modules/.vite
npm link broadcast-channel
npm run dev -- --open
```

## Troubleshooting

You may get an error when vite reloads creating the dependency cache. Refreshing the browser or closing the browser and run dev again should resolve the issue.

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

Before creating a production version of your app, install an [adapter](https://kit.svelte.dev/docs#adapters) for your target environment. Then:

```bash
npm run build
```

> You can preview the built app with `npm run preview`, regardless of whether you installed an adapter. This should _not_ be used to serve your app in production.

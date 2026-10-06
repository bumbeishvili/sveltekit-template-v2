# sveltekit-template

Starter template built on the current stable stack:

- [Svelte 5](https://svelte.dev/docs/svelte) (runes) + [SvelteKit 2](https://svelte.dev/docs/kit)
- [Vite 6](https://vite.dev)
- [Tailwind CSS 4](https://tailwindcss.com) (CSS-first config — no `tailwind.config.js`; theme lives in `src/app.css`)
- TypeScript 5.9, ESLint 9 (flat config), Prettier 3

Requires **Node 24**. Deploys to Vercel, Netlify, and other supported platforms out of the box via [`@sveltejs/adapter-auto`](https://svelte.dev/docs/kit/adapter-auto).

## Developing

Install dependencies with `npm install`, then start a development server (port 3002):

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Checks

```bash
npm run check   # svelte-check (types)
npm run lint    # prettier + eslint
npm run format  # prettier --write
```

## Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://svelte.dev/docs/kit/adapters) for your target environment.

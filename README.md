# svelte-skeleton-three-state-switch

a simple three state switch for use with skeleton in svelte 
(it can be used without skeleton you will just need to change the skeleton specific default classes)

## usage

```bash
npm install svelte-skeleton-three-state-switch
```

add the svelte-skeleton-three-state-switch content to your `tailwind.config.ts` like so
```ts
export default {
	darkMode: 'class',
	content: [
		'./src/**/*.{html,js,svelte,ts}',
		join(
			require.resolve('svelte-skeleton-three-state-switch'),
			'../**/*.{html,js,svelte,ts}'
		),
        ...
	],
	theme: {
        ...
    },
	plugins: [
        ...
    ]
};
```

it can then be imported like anything else
```ts
import { ThreeStateSwitch } from 'svelte-skeleton-three-state-switch';
```

an example is avalable in the routes directory of this project

## Developing

Once you've cloned the project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start the development server with:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

Everything inside `src/lib` is part of the library, everything inside `src/routes` is a showcase.

## Building

To build your library:

```bash
npm run package
```

To create a production version of your showcase app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

## Publishing

Go into the `package.json` and give your package the desired name through the `"name"` option.

To publish your library to [npm](https://www.npmjs.com):

```bash
npm publish
```

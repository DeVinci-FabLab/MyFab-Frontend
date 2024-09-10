# MyFab-Frontend

blabla la description

## Creating a Sveltekit project with tailwindcss

You need to have bun or npm to create a project, you can install bun here : https://bun.sh/

```bash
# create a new project in the current directory
bun create svelte@latest

# create a new project in my-app
bun create svelte@latest my-app

# Add tailwindcss 
bun install -D tailwindcss postcss autoprefixer
bun tailwindcss init -p
```

Then we need to configure tailwindcss : 

In `tailwind.config.js` : 
```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ['./src/**/**/**/*.{html,js,svelte,ts}',
  theme: {
    extend: {}
  },
  plugins: []
};
```

In `src/`, create a file named `app.css`, with this content : 
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

In `src/routes/`, create a file named `+layout.svelte`, with this content :
```svelte
<script>
	import '../app.css';
</script>

<slot />
```

> You are ready to rock !


## Developing

```bash
# init the project
git clone https://github.com/DeVinci-FabLab/MyFab-Frontend
git submodule init
git submodule update --remote --merge
bun install

# serve the project
bun run dev

# or start the server and open the app in a new browser tab
bun run dev -- --open
```

## Building

To create a production version of your app:

```bash
bun run build
```

You can preview the production build with `bun run preview`.

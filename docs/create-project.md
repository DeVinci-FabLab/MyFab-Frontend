# Creating a SvelteKit Project with TailwindCSS

> In this guide, you will learn how to create a new SvelteKit project and set up TailwindCSS for styling your application.

## Step-by-Step Guide

### 0. Prerequisites

Before you start, make sure you have `bun` installed on your system. You can install `bun` by running the following command:

```bash
npm install -g @bun/cli
```

Or use the package manager appropriate for your system (more info on the [official docs](https://bun.sh)).

### 1. Create a New SvelteKit Project

First, you need to create a new SvelteKit project. You can do this by running the following commands:

```bash
# Create a new project in the current directory
bun create svelte@latest

# Create a new project in a directory named 'my-app'
bun create svelte@latest my-app
```

### 2. Install TailwindCSS

Next, you need to install TailwindCSS and its dependencies. Run the following commands:

```bash
# Install TailwindCSS, PostCSS, and Autoprefixer
bun install -D tailwindcss postcss autoprefixer

# Initialize TailwindCSS with PostCSS
bun tailwindcss init -p
```

### 3. Configure TailwindCSS

After installing TailwindCSS, you need to configure it. Update the `tailwind.config.js` file with the following content:

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ['./src/**/**/**/*.{html,js,svelte,ts}'],
  theme: {
    extend: {}
  },
  plugins: []
};
```

### 4. Create the TailwindCSS File

Create a new file named `app.css` in the `src/` directory with the following content:

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 5. Import TailwindCSS in Your SvelteKit Project

Create a new file named `+layout.svelte` in the `src/routes/` directory with the following content:

```svelte
<script>
  import '../app.css';
</script>

<slot />
```

## You're Ready to Rock

With these steps, you have successfully set up a SvelteKit project with TailwindCSS. You can now start building your application with the power of SvelteKit and the styling capabilities of TailwindCSS.

---

**Document Last Updated**: September 2024

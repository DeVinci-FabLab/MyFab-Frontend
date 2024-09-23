# Developing and Building Your SvelteKit Project

> In this guide, you will learn how to set up your development environment, develop your SvelteKit project, and build it for production.

## Step-by-Step Guide

### 0. Prerequisites

Before you start, make sure you have the following installed on your system:

- **Git**: For version control.
- **Bun**: A fast JavaScript runtime. You can install `bun` by running the following command:

  ```bash
  npm install -g @bun/cli
  ```

  Or use the package manager appropriate for your system (more info on the [official docs](https://bun.sh)).

### 1. Clone the Project

First, you need to clone the project repository and initialize its submodules:

```bash
# Clone the repository
git clone https://github.com/DeVinci-FabLab/MyFab-Frontend

# Navigate to the project directory
cd MyFab-Frontend
```

### 2. Install Dependencies

Next, install the project dependencies using `bun`:

```bash
bun install
```

### 3. Set Up Visual Studio Code Environment

To enhance your development experience, you can set up Visual Studio Code with the following extensions:

- **Svelte**: Provides syntax highlighting and other features for Svelte files.
- **Prettier - Code formatter**: For consistent code formatting.
- **ESLint**: For linting JavaScript and TypeScript code.

You can install these extensions by searching for them in the Visual Studio Code Extensions Marketplace.

Additionally, you can configure your workspace settings by creating a `.vscode` folder in the root of your project and adding a `settings.json` file with the following content:

```json
{
  "editor.formatOnSave": true,
  "prettier.requireConfig": true,
  "eslint.validate": ["javascript", "javascriptreact", "svelte", "typescript", "typescriptreact"],
  "svelte.enable-ts-plugin": true
}
```

### 4. Developing

To start the development server, run the following command:

```bash
# Serve the project
bun run dev
```

You can also start the server and open the app in a new browser tab by running:

```bash
bun run dev -- --open
```

### 5. Building

To create a production version of your app, run the following command:

```bash
bun run build
```

You can preview the production build with:

```bash
bun run preview
```

## You're Ready to Rock

With these steps, you have successfully set up your development environment, developed your SvelteKit project, and built it for production. You can now start building your application with the power of SvelteKit and the enhanced development experience provided by Visual Studio Code.

---

**Document Last Updated**: September 2024

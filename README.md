# Vite Frontend App with GitHub Actions Caching

This repository provides a Vite frontend app that demonstrates how to use GitHub Actions to cache the `node_modules` folder, speeding up the build process and reducing dependencies download time.

## Prerequisites

Before getting started, ensure you have the following prerequisites installed:

- [Node.js](https://nodejs.org) (version 12 or higher)
- [npm](https://www.npmjs.com/) or [Yarn](https://yarnpkg.com/)

## Getting Started

Follow these steps to set up and run the Vite frontend app:

1. **Clone the repository**:

   ```bash
   git clone https://github.com/your-username/vite-frontend-app.git
   ```

2. **Navigate to the project directory**:

   ```bash
   cd vite-frontend-app
   ```

3. **Install dependencies**:

   If you're using npm:

   ```bash
   npm install
   ```

   If you're using Yarn:

   ```bash
   yarn
   ```

4. **Start the development server**:

   If you're using npm:

   ```bash
   npm run dev
   ```

   If you're using Yarn:

   ```bash
   yarn dev
   ```

   The app will be running at `http://localhost:3000`.

## GitHub Actions Workflow

This repository includes a preconfigured GitHub Actions workflow that demonstrates how to cache the `node_modules` folder to speed up subsequent builds. Here's how it works:

1. Whenever a pull request is opened or pushed to the repository, the workflow triggers.

2. The workflow installs dependencies, caches the `node_modules` folder, and runs the build step.

3. On subsequent runs, the workflow checks if the cache is available. If it is, it restores the `node_modules` folder from cache, skipping the dependency installation step. This significantly reduces the build time.

To use the GitHub Actions workflow in your own projects, follow these steps:

1. **Copy the workflow file**:

   Copy the `.github/workflows/cache-node-modules.yml` file from this repository to the corresponding location in your project repository.

2. **Commit and push the changes**:

   Commit and push the copied workflow file to your project repository.

3. **Configure the workflow**:

   If needed, customize the workflow file to fit your specific project requirements.

4. **Enable GitHub Actions**:

   Enable GitHub Actions in your project repository. The workflow will now be triggered automatically whenever a pull request is opened or pushed.

## Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please [create an issue](https://github.com/your-username/vite-frontend-app/issues) or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

---

Enjoy building and caching your Vite frontend app using GitHub Actions! If you have any questions, feel free to reach out to the project maintainer or create an issue in the repository. Happy coding!


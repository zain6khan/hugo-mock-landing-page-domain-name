# hugo-mock-landing-page
This repository is set up with a GitHub Actions workflow to automatically build and deploy my Hugo website for the product FitnessFriend to GitHub Pages whenever changes are pushed to the `main` branch.

The workflow file (`.github/workflows/hugo.yml`) contains the following steps:

1. **Check Out Source Repository**: Checks out the repository code, including submodules (e.g., Hugo themes) and fetches the entire commit history (required for certain Hugo features like `.GitInfo` and `.Lastmod`).

2. **Initialize Hugo Environment**: Sets up the Hugo environment using a specific version (`0.123.4`) and enables the extended mode (required for certain Hugo features).

3. **Compile Hugo Static Files**: Runs the `hugo` command to build the static files for the website, including draft content, garbage collection, and minification.

4. **Publish to GitHub Pages**: Publishes the built files to the `gh-pages` branch, which is used by GitHub Pages to serve the website at `https://zain6khan.github.io/hugo-mock-landing-page-autodeployed/`.

After any push to the `main` branch, the workflow will automatically trigger and deploy the latest changes to the live website. This streamlines the deployment process and ensures that the website is always up-to-date with the latest content and changes.

You can view the workflow runs and their status in the "Actions" tab of this repository. If a workflow run fails, you can inspect the logs to identify and fix any issues.
